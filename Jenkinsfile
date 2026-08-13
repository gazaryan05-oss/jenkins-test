pipeline {
    agent any

    tools {
        sonarRunner 'SonarScanner'
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