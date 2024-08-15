pipeline {
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/dungdt-dev/hello-nodejs2.git'
            }
        }

        stage('Build image') {
            steps {
                sh 'docker build -t dungdt24042/demo-nodejs:v1 .
            }
        }
    }
}