pipeline {
    agent any 

    stages {        
        stage('Construccion') {
            steps {
               sh 'cp .env.example .env'
               sh 'composer install'
               sh 'php artisan key:generate'
               sh 'php artisan migrate'
               sh 'php artisan db:seed'
            }
        }
        stage('Tests') {
            steps {
               sh "chmod +x -R ${env.WORKSPACE}"
               sh './vendor/bin/phpunit'
            }
        }
    }   
}