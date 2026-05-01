pipeline {
    agent any 

    stages {
        
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Lopez0912/DevOps-Lab.git'
            }
        }

        stage('Build') {
            steps {
                sh 'docker build -t lopez0912/devops-app .'
            }
        }

        stage('Push') {
            steps {
                withCredentials([string(credentialsId: 'docker-pass', variable: 'PASS')]) {
                    sh "echo $PASS | docker login -u lopez0912 --password-stdin"
                    sh 'docker push lopez0912/devops-app'
                }
            }
        }

        stage('Deploy') {
            steps {
                sh 'kubectl apply -f k8s/'
            }
        }
    }
}