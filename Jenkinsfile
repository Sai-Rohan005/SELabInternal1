pipeline {
    agent any
    tools {
        maven 'Maven3'
    }
    stages {
        stage('git repo & clean') {
            steps {
                script {
                    // Only clean, no need to clone again
                    sh 'mvn clean'
                }
            }
        }
        stage('install') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'mvn install'
                    } else {
                        bat 'mvn install'
                    }
                }
            }
        }
        stage('test') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'mvn test'
                    } else {
                        bat 'mvn test'
                    }
                }
            }
        }
        stage('package') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'mvn package'
                    } else {
                        bat 'mvn package'
                    }
                }
            }
        }
    }
}
