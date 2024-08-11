pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/dungdt-dev/hello-nodejs2.git'
            }
        }

        stage('build image') {
            steps {
                 sshagent (credentials: ['server-key']) {
                    sh 'ssh -o StrictHostKeyChecking=no -l ec2-user 18.139.223.247 uname -a touch test.txt'
                  }
            }
        }

    }
}