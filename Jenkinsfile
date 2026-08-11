pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building Java application...'
                bat 'mvn clean package -DskipTests'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Java web application...'
                echo 'Deployment completed successfully!'
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline completed successfully!'
        }

        failure {
            echo 'CI/CD Pipeline failed!'
        }
    }
}