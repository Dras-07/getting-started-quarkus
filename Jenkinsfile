pipeline {
    agent any 
    stages {
        stage('Start') {
            steps {
                echo 'build'
            }
        }
        
        stage('install'){
            stage{
             sh   'mvn -U clean install'

            }
        }
    }
}
