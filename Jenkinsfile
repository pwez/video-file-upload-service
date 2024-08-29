pipeline {
    agent any

    stages {
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
        stage('SonarQube Scan') {
            steps {
                sh './gradlew sonarqube'
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
