pipeline {
    agent any 
    stages {
        stage('Start') {
            steps {
                echo 'build1'
                  }
                        }
        
        stage('install'){
            steps{
             sh   'mvn -U clean install'
                 }
        }
     
        
    stage ('Docker image build'){
      
        steps{ 
       sh    'docker build -f src/main/docker/Dockerfile.jvm -t quarkus/getting-started-reactive-jvm .'
             }
         } 
        stage ('Deploying') {
      steps {
       sh  'docker run -i --rm -p 8080:8080 quarkus/getting-started-reactive-jvm'
        sh 'echo deploying'
           }
                           }
    }
                   
}
