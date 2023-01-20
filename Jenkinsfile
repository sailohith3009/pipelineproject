pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
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
                sh 'docker run -itd -p 8081:80 vedacode/customnginx'
            }
        }
        stage('pipeline') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
