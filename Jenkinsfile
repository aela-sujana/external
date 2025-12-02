pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/aela-sujana/external.git'
            }
        }

        stage('Build') {
            steps {
                bat 'echo Building project...'
                bat 'gradlew build'
            }
        }

        stage('Test') {
            steps {
                bat 'echo Running tests...'
                bat 'gradlew test'
            }
        }

        stage('Deploy') {
            steps {
                bat 'echo Deploying application...'
                // Add your Windows deploy commands here
            }
        }
    }
}
