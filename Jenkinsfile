pipeline {
    agent any

    tools {
        jdk 'Java 17'
    }

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
