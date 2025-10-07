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
                        sh "git clone https://your-github-link"
                        sh "mvn clean -f mavenjava"
                    } else {
                        bat "git clone https://your-github-link"
                        bat "mvn clean -f mavenjava"
                    }
                }
            }
        }
        stage('install') {
            steps {
                script {
                    if (isUnix()) {
                        sh "mvn install -f mavenjava"
                    } else {
                        bat "mvn install -f mavenjava"
                    }
                }
            }
        }
        stage('test') {
            steps {
                script {
                    if (isUnix()) {
                        sh "mvn test -f mavenjava"
                    } else {
                        bat "mvn test -f mavenjava"
                    }
                }
            }
        }
        stage('package') {
            steps {
                script {
                    if (isUnix()) {
                        sh "mvn package -f mavenjava"
                    } else {
                        bat "mvn package -f mavenjava"
                    }
                }
            }
        }
    }
}
