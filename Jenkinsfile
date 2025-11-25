pipeline {
    agent any

    stages {
        stage('git clone') {
            steps {
               //bat rmi /s /q MavenJavaDemo
               bat "git clone https://github.com/Sai-Rohan005/SELabinternal1.git"
               bat "mvn clean -f SELabInternal1"
            }
        }
        stage('install') {
            steps {
               bat "mvn install -f SELabInternal1"
            }
        }
        stage('test'){
            steps{
                bat "mvn test -f SELabInternal1"
            }
            
        }
    }
}
