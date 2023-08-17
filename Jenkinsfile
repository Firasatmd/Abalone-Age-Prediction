pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                sh 'sudo docker build -t python-img1 .'
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'sudo docker run -d -p 8082:8082 python-img1'
            }
        }
    }   
}
