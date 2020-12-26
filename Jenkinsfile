pipeline {
    agent any 

    stages {        
        stage('Test') {
            steps {
               sh 'cp .env.example .env'
               sh 'composer install'
            }
        }
    }   
}