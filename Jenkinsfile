pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/gehlot26/CICD-practice.git'
            }
        }
        stage('Build') {
            steps {
                sh './mvnw clean install'  // Use wrapper if available
                // sh 'mvn clean install'  // Use if no wrapper
            }
        }
        stage('Test') {
            steps {
                sh './mvnw test'  // Use wrapper if available
                // sh 'mvn test'  // Use if no wrapper
            }
        }
        stage('Package') {
            steps {
                sh './mvnw package'  // Use wrapper if available
                // sh 'mvn package'  // Use if no wrapper
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Example deployment command or script
            }
        }
    }
    post {
        success {
            echo 'Build and deployment succeeded!'
        }
        failure {
            echo 'Build or deployment failed.'
        }
    }
}
