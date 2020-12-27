pipeline {
    agent any 

    stages {        
        stage('Construccion') {
            steps {
               sh 'cp .env.example .env'
               sh 'composer install'
               sh 'php artisan key:generate'
               sh 'php artisan migrate'
            }
        }
        stage('Tests') {
            steps {
               sh "chmod +x -R ${env.Pipeline}"
               sh './vendor/bin/phpunit'
            }
        }
    }   
}