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
             post {
    success {
      mail to: anjanays619@gmail.com, subject: ‘The Pipeline success :(‘
            }
                  }
                      }
           }
}
