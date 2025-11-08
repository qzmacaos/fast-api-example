pipeline {
    agent any
    stages {
        stage('checkout'){
            steps {
                git branch: 'main', url: 'https://github.com/qzmacaos/fast-api-example.git'
            }
        }
        stage('build'){
            steps {
                script {
                    dockerImage = docker.build("fast-api-example:latest")
                }
            }
        }
        stage('test'){
            steps {
                sh 'docker run --rm fast-api-example:latest pytest'
            }
        }
    }
}