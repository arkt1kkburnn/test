pipeline {
    agent any  // Используем любой доступный агент Jenkins

    stages {
        stage('Checkout') {
            steps {
                // Подключение к Git
                git branch: 'main', url: 'https://github.com/arkt1kkburnn/test'
            }
        }

        stage('Build') {
            steps {
                // Здесь команды сборки, например
                sh 'echo "Сборка проекта..."'
            }
        }

        stage('Test') {
            steps {
                // Запуск тестов
                sh 'echo "Запуск тестов..."'
            }
        }
    }

    post {
        success {
            echo "✅ Пайплайн успешно выполнен"
        }
        failure {
            echo "❌ Пайплайн упал"
        }
    }
}
