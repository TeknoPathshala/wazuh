pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout your project repository
                checkout scm
            }
        }
        
        stage('Build and Deploy') {
            steps {
                // Use Docker Compose to start ELK stack and Wazuh server
                sh 'docker-compose -f docker-compose.yml up -d'
            }
        }
    }
}
