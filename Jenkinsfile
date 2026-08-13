pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building project...'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('sonar-scanner-server') {
                    sh 'sonar-scanner -Dsonar.projectKey=my-project -Dsonar.sources=.'
                }
            }
        }
    }
}