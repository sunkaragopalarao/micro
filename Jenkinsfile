pipeline {
    agent any

    stages {
        stage('Build & Tag Docker Image') {
            steps {
                script {
                    withDockerRegistry(credenti adijaiswalalsId: 'docker-cred', toolName: 'docker') {
                        sh "docker build -t sunkaragopalarao/frontend:latest ."
                    }
                }
            }
        }
        
        stage('Push Docker Image') {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'docker-cred', toolName: 'docker') {
                        sh "docker push asunkaragopalarao/frontend:latest"
                    }
                }
            }
        }
    }
}
