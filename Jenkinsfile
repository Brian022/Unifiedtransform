pipeline {
    agent any 

    stages {
        stage('Prepare') {
            steps {
                sh 'cp .env.example .env'
                sh 'composer install'
            }
        }
        
        stage('Test') {
            steps {
               sh './vendor/bin/phpunit'
            }
        }
    }   
}