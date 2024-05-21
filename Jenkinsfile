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
        
        
    }
}
