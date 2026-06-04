pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/AICHAAITDOUCH/tp-devops-laravel.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'composer install'
            }
        }

        stage('Laravel Check') {
            steps {
                sh 'php artisan --version'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'php artisan test'
            }
        }
    }
}