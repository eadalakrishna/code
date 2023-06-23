pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clean workspace before checking out
                cleanWs()
                
                // Checkout the Git repository
                git branch: 'test', url: 'https://github.com/jetopsB055/code'
            }
        }
        
        stage('Build') {
            steps {
                // Add your build steps here. just adding in a comment
                // For example, if you're using npm to build the JavaScript project:
                sh 'npm install'
                sh 'npm run build'
            }
        }
        
        stage('Test') {
            steps {
                // Add your test steps here
                // For example, if you're using npm to run tests:
                sh 'npm test'
            }
        }
        
        stage('Deploy') {
            steps {
                // Add your deployment steps here
                // For example, if you're using npm to deploy:
                sh 'npm run deploy'
            }
        }
    }
}

