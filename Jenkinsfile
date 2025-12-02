pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
        
                git branch: 'master',
                    url: 'https://github.com/aela-sujana/external.git'
            }
        }

        stage('Build') {
            steps {
                // Example build step
                sh 'echo "Building project..."'
                sh './gradlew build'   
            }
        }

        stage('Test') {
            steps {
                // Example test step
                sh 'echo "Running tests..."'
                sh './gradlew test'    
            }
        }

        stage('Deploy') {
            steps {
                // Example deploy step
                sh 'echo "Deploying application..."'
                
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
