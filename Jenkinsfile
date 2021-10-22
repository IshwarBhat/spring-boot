pipeline {
    agent any

    triggers {
        pollSCM 'H/15 * * * *'
    }
    stages {
        stage('Build') {
            steps {
                sh './gradlew assemble'
            }
        }
        stage('Test') {
            steps {
                sh './gradlew test'
            }
        }
        stage('Scan') {
            steps {
                echo 'Veracode Scan ...'
            }
        }
    }
}