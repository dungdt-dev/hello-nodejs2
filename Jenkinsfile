pipeline {
    agent any

    environment {
        REPO_URL = 'https://github.com/dungdt-dev/hello-nodejs2.git' // URL của repository
        DOCKER_IMAGE = 'dungdt24042/demo-nodejs'
        BUILD_NUMBER = 'v1'
    }

    stages {
        stage('Clone code') {
            steps {
                git branch: 'master', url: "${REPO_URL}"
            }
        }

        stage('Build Docker image') {
            steps {
                script {
                    // Build Docker image
                    def image = docker.build("${DOCKER_IMAGE}:${BUILD_NUMBER}")


                }
            }
        }
    }

    post {
        always {
            cleanWs()
        }
    }
}
