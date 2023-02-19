pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o jags PES1UG20CS650.cpp'
                build job : 'PES1UG20CS650-1'
                echo 'Build stage successful'
            }
        }
        stage('Test') {
            steps {
                sh './jagzz'
                echo 'Test stage successful'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying "'
                echo 'Deployment successful'
            }
        }
    }
    post {
        failure {
          echo 'Pipeline failed'
                }
            
        
    }
}
