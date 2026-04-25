pipeline {
    agent any
    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main' , url: 'https://github.com/Satwik-Harpale/CI-CD-Jenkins.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t event-registration-app .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 5000:5000 event-registration-app'
            }
        }

        stage('Test Application') {
            steps {
                echo 'Application Deployed Successfully'
            }
        }
    }
}