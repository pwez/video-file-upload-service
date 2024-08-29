pipeline {
    agent any

    stages {
        stage('Build Repository') {
            steps {
                sh 'echo'
                sh 'echo -------------------'
                sh 'echo Building Repository'
                sh './gradlew build'
            }
        }
        stage('Run Unit Tests') {
            steps {
                sh 'echo'
                sh 'echo -------------------'
                sh 'echo Running Unit Tests'
                sh './gradlew test'
            }
        }
        stage('SonarQube Scan') {
            steps {
                sh 'echo'
                sh 'echo -------------------'
                sh 'echo Running SonarQube Scan'
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
