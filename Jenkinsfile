pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('this') {
            steps {
                sh '''docker build -t vedacode/customnginx .
                docker run -itd vedacode/customnginx '''
            }
        }
        stage('is') {
            steps {
                echo 'Hello World'
            }
        }
        stage('pipeline') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
