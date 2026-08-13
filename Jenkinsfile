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
                withSonarQubeEnv('SonarQube') {   // ← Имя из настроек
                    sh 'sonar-scanner -Dsonar.projectKey=my-project -Dsonar.sources=.'
                }
            }
        }
    }
}
