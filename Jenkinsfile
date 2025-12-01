pipeline {
    agent any

    tools {
        maven 'maven3'  // Make sure this matches your Jenkins Maven tool name
    }

    stages {
        stage('Welcome') {
            steps {
                echo "Welcome to Jenkins portol !"
            }
        }

        stage('Clean') {
            steps {
                bat "mvn clean -f ."
            }
        }

        stage('Install') {
            steps {
                bat "mvn install"
            }
        }

        stage('Test') {
            steps {
                bat "mvn test"
            }
        }

        stage('Package') {
            steps {
                bat "mvn package"
                echo "Build Number: ${env.BUILD_NUMBER}"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment steps go here."
            }
        }
    }
}
