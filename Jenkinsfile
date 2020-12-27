pipeline {
    agent any 

    stages {        
        stage('Construccion') {
            steps {
               sh 'cp .env.example .env'
               sh 'composer install'
            }
        }
        stage('Tests') {
            steps {
               sh 'chmod +x -R ${env.WORKSPACE}'
               sh './vendor/bin/phpunit'
            }
        }
    }   
}