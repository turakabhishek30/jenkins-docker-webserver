pipeline {
    agent any
    stages {
        stage('Pull Docker Image') {
            steps {
                script {
                    sh 'docker pull nginx:latest' // Replace nginx with your custom image if needed
                }
            }
        }
        stage('Run Web Server') {
            steps {
                script {
                    sh 'docker run -d -p 8080:80 nginx:latest' // Map port 8080 to 80
                }
            }
        }
        stage('Test Web Server') {
            steps {
                script {
                    sh 'curl http://localhost:8080' // Verify the server is running
                }
            }
        }
    }
}
