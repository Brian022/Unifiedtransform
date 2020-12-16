pipeline {
    agent any 

    stages {
        stage('Prepare') {
            steps {
                sh 'cp .env.example .env'
                sh 'sudo apt composer install'
                sh 'composer install'
                sh 'composer install --optimize-autoloader --no-dev'
            }
        }
        
        stage('Test') {
            steps {
               sh './vendor/bin/phpunit'
            }
        }
    }   
}