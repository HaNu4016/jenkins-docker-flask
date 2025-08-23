pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/HaNu4016/jenkins-docker-flask.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t jenkins-docker-flask .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 jenkins-docker-flask || true'
            }
        }
    }
}

