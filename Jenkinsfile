pipeline {
    agent any

    stages {
        stage('Build Repository') {
            steps {
                sh 'echo'
                sh './gradlew build'
            }
        }
        stage('Run Unit Tests') {
            steps {
                sh 'echo'
                sh './gradlew test'
            }
        }
        stage('SonarQube Scan') {
            steps {
                sh 'echo'
                sh './gradlew sonar'
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
