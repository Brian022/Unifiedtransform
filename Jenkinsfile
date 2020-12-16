pipeline {
    agent any 

    stages {
        stage('Prepare') {
            steps {
                sh 'cp .env.example .env'
                sh './docker-install.sh'
            }
        }
        
        stage('Test') {
            steps {
               sh './vendor/bin/phpunit'
            }
        }
    }   
}