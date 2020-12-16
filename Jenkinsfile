pipeline {
    agent any 

    stages {
        stage('Prepare') {
            steps {
                sh 'git clone https://github.com/Brian022/Unifiedtransform.git'
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