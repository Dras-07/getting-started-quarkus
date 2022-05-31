pipeline {
    agent any 
    stages {
        stage('Start') {
            steps {
                echo 'build'
                  }
                        }
        
        stage('install'){
            steps{
             sh   'mvn -U clean install'
                 }
        }
        
        
    stage ('Docker image build'){
        steps{
                echo 'Building docker image'
             }
        steps{
                    sh 'docker build -t Dockerfile .'
             }
                } 
        stage ('Deploying') {
      steps {
        sh 'echo deploying'
           }
                           }
    }
                   
}
