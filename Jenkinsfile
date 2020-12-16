pipeline {
    agent any 

    stages {
        stage('Prepare') {
            steps {
                sh '/personalProjects/Prubea/composer install'
                sh 'cp .env.example .env'
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