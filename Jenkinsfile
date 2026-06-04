pipeline {
    agent any

    stages {

        stage(' Préparation (Setup)') {
            steps {
                sh 'cp -n .env.example .env || true'
            }
        }

        stage(' Installation') {
            steps {
                sh 'composer install'
                sh 'php artisan key:generate'
            }
        }

        stage(' Tests') {
            steps {
                sh 'php artisan test'
            }
        }

    }
}