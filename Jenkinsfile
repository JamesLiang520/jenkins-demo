pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checkout source code'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Building application..."'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "Running tests..."'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploying application..."'
            }
        }
    }

    post {
        success {
            echo '✅ Pipeline success'
        }
        failure {
            echo '❌ Pipeline failed'
        }
    }
}
