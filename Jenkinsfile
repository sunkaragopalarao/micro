pipeline {
    agent any

    stages {
        stage('Deploy To Kubernetes') {
            steps {
                withKubeCredentials(kubectlCredentials: [[caCertificate: '', clusterName: 'EKS-1', contextName: '', credentialsId: 'kube-token', namespace: 'webapps', serverUrl: 'https://411DCC32CC5B5B0C3BE0FBDAABACDB7A.gr7.ap-south-1.eks.amazonaws.com']]) {
                
                
                 sh "kubectl apply -f deployment-service.yml"
              }
            }
        }
        
        
        stage('Hello') {
            steps {
                withKubeCredentials(kubectlCredentials: [[caCertificate: '', clusterName: 'EKS-1', contextName: '', credentialsId: 'kube-token', namespace: 'webapps', serverUrl: 'https://411DCC32CC5B5B0C3BE0FBDAABACDB7A.gr7.ap-south-1.eks.amazonaws.com']]) {
                   
                    sh "kubectl get svc -n webapps"
  
  
                   
                }
            }
        }
        
    }
}
