pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'master',
                    credentialsId: '339c54bb-8b57-4f11-9f66-2cfa5f33d5a9',
                    url: 'git@github.com:balasahebjavheri-devops/devops-day2-git-practice.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t balasahebjavheri1995/akshay-devops-app:pipeline .'
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'docker push balasahebjavheri1995/akshay-devops-app:pipeline'
            }
        }
    }
}

