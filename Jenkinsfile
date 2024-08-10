pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/dungdt-dev/hello-nodejs2.git'
            }
        }

        stage('Clone') {
            steps {
                withDockerRegistry(credentialsId: 'docker-hub', url: ' https://index.docker.io/v1/') {
                    sh 'docker build -t dungdt24042/demo-nodejs:v1 .'
                    sh 'docker push dungdt24042/demo-nodejs:v1 .'
                }
            }
        }

    }
}