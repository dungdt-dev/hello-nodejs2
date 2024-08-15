pipeline {
    agent {
        docker {
            image 'docker:dind'
            args '-u root:root -p 3000:3000 --privileged -v /var/run/docker.sock:/var/run/docker.sock'
        }
    }

    environment {
        CI = 'true'
    }

    stages {
    stage('Clone') {
        steps {
            git 'https://github.com/dungdt-dev/hello-nodejs2.git'
            }
        }
        stage('docker build') {
            when {
                branch 'master'
            }
            steps {
                sh 'docker build -t dungdt24042/demo-nodejs:v1'
            }
        }
    }
}