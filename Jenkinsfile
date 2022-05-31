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
           
           }
}
