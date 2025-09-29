pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/arkt1kkburnn/test.git',
                    credentialsId: 'github-token'
            }
        }
        stage('Build') {
            steps {
                bat 'echo Сборка проекта...'
            }
        }
        stage('Test') {
            steps {
                bat 'echo Тесты проходят...'
            }
        }
    }

    post {
        success {
            echo "✅ Пайплайн выполнен успешно!"
        }
        failure {
            echo "❌ Пайплайн завершился с ошибкой!"
        }
    }
}
