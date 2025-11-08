pipeline {
    agent { docker { image 'python:3.11-slim' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
    }
    post {
        always {
            echo 'try'
        }
        success {
            echo 'ok'
        }
        failure {
            echo 'fail'
        }
    }
}