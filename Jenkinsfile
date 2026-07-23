pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                echo 'Starting Docker build...'
                sh 'docker build -t my-jenkins-app:latest .'
                echo 'Docker build completed!'
            }
        }
    }
}
