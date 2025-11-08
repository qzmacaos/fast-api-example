pipeline {
    agent { docker { build '.' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
        stage('test') {
            steps {
                sh 'pytest'
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