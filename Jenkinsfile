pipeline{
    agent any
    stages{
        stage('Clone repo'){
            steps{
                git branch: 'main', url: 'https://github.com/prashantgohel321/DevOps-Project-Two-Tier-Flask-App.git'
            }
        }
        stage('Build image'){
            steps{
                sh 'docker build -t flask-app .'
            }
        }
        stage('Deploy with docker compose'){
    steps{
        sh 'export PATH=$PATH:/usr/local/bin:/usr/bin && docker-compose down || true'
        sh 'export PATH=$PATH:/usr/local/bin:/usr/bin && docker-compose up -d --build'
    }
}
    }
}
