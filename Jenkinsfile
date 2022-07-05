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
     
        
    stage ('Docker image build 1'){
      
        steps{ 
            //sh  'docker build -f src/main/docker/Dockerfile.native -t quarkus/getting-started-reactive .'
            sh ' docker build -f src/main/docker/Dockerfile.jvm -t quarkus/getting-started-reactive-jvm .'
            //sh 'docker build -f src/main/docker/Dockerfile.native -t quarkus/getting-started-reactive .'
             }
        }
        
//          stage ('Docker image build 2'){
      
//         steps{ 
//        sh   ' docker build -f src/main/docker/Dockerfile.legacy-jar -t quarkus/getting-started-reactive-legacy-jar .'
//              }
//          } 
      
        stage ('RUN IMAGE') {
      steps {
       sh  'docker run -d  --rm -p 8010:8080 quarkus/getting-started-reactive-jvm'
        sh 'echo deploying'
           }
                           }
    }
                   
}
