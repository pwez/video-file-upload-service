pipeline {
    agent any

    stages {
        stage('Checkout Repository') {
            steps {
                checkout scm
            }
        }
        stage('Build Repository') {
            steps {
                sh './gradlew build'
            }
        }
        stage('Run Unit Tests') {
            steps {
                sh './gradlew test'
            }
        }

    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
