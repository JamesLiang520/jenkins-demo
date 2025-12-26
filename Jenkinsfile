pipeline {
    agent any

    parameters {
        choice(
            name: 'ENV',
            choices: ['dev', 'test', 'prod'], // 默认值 = 第一个 = dev
            description: 'Deployment environment'
        )
    }

    stages {
        stage('Checkout') {
            steps {
                echo '🔄 Checkout source code'
            }
        }

        stage('Build') {
            steps {
                echo '🏗 Build stage'
                sh "echo Building for environment: ${params.ENV}"
            }
        }

        stage('Test') {
            steps {
                echo '🧪 Test stage'
                sh "echo Testing for environment: ${params.ENV}"
            }
        }

        stage('Deploy') {
            steps {
                echo "🚀 Deploy stage"
                sh "echo Deploying to environment: ${params.ENV}"
            }
        }
    }

    post {
        success {
            echo '✅ Pipeline SUCCESS'
        }
        failure {
            echo '❌ Pipeline FAILED'
        }
    }
}
