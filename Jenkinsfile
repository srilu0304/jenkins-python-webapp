pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/YOUR_USERNAME/jenkins-python-webapp.git'
            }
        }
        stage('Install Requirements') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Run Web App') {
            steps {
                sh 'nohup python app.py &'
            }
        }
        stage('Ping Web App') {
            steps {
                sh 'curl http://localhost:5000'
            }
        }
    }
}
