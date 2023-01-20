pipeline {
    agent any

    stages {
        stage('Remove all containers') {
            steps {
                sh 'docker ps -aq | xargs docker stop | xargs docker rm'
            }
        }
        stage('docker build') {
            steps {
                sh '''docker build -t vedacode/customnginx .
                '''
            }
        }
        stage('docker run') {
            steps {
                sh 'docker run -itd -p 8081:80 --name=mynginx vedacode/customnginx'
            }
        }
        stage('pipeline') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
