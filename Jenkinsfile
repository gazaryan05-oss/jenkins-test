pipeline {
    agent any

    tools {
        sonarQube 'SonarScanner'   // имя из Global Tool Configuration
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building project...'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('sonar-scanner-server') {   // ← твоё имя сервера!
                    sh 'sonar-scanner -Dsonar.projectKey=my-project -Dsonar.sources=.'
                }
            }
        }
    }
}