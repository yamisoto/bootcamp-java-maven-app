pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Checkout code from your Git repository
                git url: 'https://github.com/yamisoto/bootcamp-java-maven-app.git', branch: 'jenkins-jobs'
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building the application...'
                // If you're using Maven for building, add Maven build steps here
                // For example:
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // If you have tests, run them with Maven
                // For example:
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Add deployment steps here
                // For example, you can use a script or tool to deploy the built application
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed.'
        }
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}

