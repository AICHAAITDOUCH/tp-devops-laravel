pipeline {
    agent any

    stages {

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