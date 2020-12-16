pipeline {
    agent any 

    stages {
        stage('Prepare') {
            steps {
                sh 'git clone https://github.com/changeweb/Unifiedtransform'
                sh 'cp .env.example .env'
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