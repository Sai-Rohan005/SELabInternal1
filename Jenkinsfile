pipeline {
    agent any
    tools {
        maven 'Maven3'
    }
    stages {
        stage('git repo & clean') {
            steps {
                script {
                    if (isUnix()) {
                        sh "git clone https://github.com/Sai-Rohan005/SELabInternal1.git"
                        sh "mvn clean"
                    } else {
                        bat "git clone https://github.com/Sai-Rohan005/SELabInternal1.git"
                        bat "mvn clean"
                    }
                }
            }
        }
        stage('install') {
            steps {
                script {
                    if (isUnix()) {
                        sh "mvn install"
                    } else {
                        bat "mvn install"
                    }
                }
            }
        }
        stage('test') {
            steps {
                script {
                    if (isUnix()) {
                        sh "mvn test"
                    } else {
                        bat "mvn test"
                    }
                }
            }
        }
        stage('package') {
            steps {
                script {
                    if (isUnix()) {
                        sh "mvn package"
                    } else {
                        bat "mvn package"
                    }
                }
            }
        }
    }
}
