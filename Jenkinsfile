pipeline{
    agent {label 'kube-master'}
    stages{
        stage('SCM'){
            steps{
                git branch:'main', url:'https://github.com/Agasthyahm/kube-app-deploy.git'
            }
        }
        stage('Deploy Service'){
            steps{
                sh 'kubectl apply -f np-svc.yaml'
            }
        }
        stage('Deploy pods'){
            steps{
                sh 'kubectl apply -f dep.yaml'
            }
        }
    }
}
