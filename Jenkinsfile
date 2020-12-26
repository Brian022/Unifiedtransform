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
               sh '/var/lib/jenkins/workspace/Pipeline'
               sh './vendor/bin/phpunit'
            }
        }
    }   
}