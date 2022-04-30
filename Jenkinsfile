pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                // checkout code from a GitHub repository
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-cred', url: 'https://github.com/morapost/locus-assignment-app/']]])
            }
            
        }
        stage('Build Environment') {
            steps {
                sh 'python3 -m venv django-app'
                sh 'source django-app/bin/activate'
            }
        }
        stage('Install Requirements') {
            steps {
                sh 'python3 -m pip install -r requirements.txt'
            }
        }
    }
}
