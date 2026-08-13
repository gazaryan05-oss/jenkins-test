
pipeline {
    agent any

    tools {
        sonarQube 'SonarScanner'   // добавляем эту строку
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building project...'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('SonarQube') {
                    sh 'sonar-scanner -Dsonar.projectKey=my-project -Dsonar.sources=.'
                }
            }
        }
    }
}