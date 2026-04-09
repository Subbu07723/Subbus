pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Subbu07723/Laksh.git'
            }
        }

        stage('Deploy to EKS') {
            steps {
                sh '''
                kubectl apply -f deployment.yaml
                kubectl apply -f service.yaml
                '''
            }
        }
    }
}
