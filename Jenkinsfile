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
               sh 'cd ..'
               sh 'cd Pipeline'
               sh './vendor/bin/phpunit'
            }
        }
    }   
}