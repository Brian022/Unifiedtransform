pipeline {
    agent any 

    stages {        
        stage('Construccion') {
            steps {
               sh 'cp .env.example .env'
               sh 'composer install'
               sh 'php artisan key:generate'
               sh 'php artisan migrate'
            }
        }
        stage('Sonarqube') {
            steps{
                echo 'Problemas con Java'
            }
        }
        stage('Tests') {
            steps {
               sh "chmod +x -R ${env.Workspace}"
               sh './vendor/bin/phpunit'
            }
        }

        stage('Conteinarizacion') {
            steps {
               sh 'cp .env.example .env'
               sh './docker-install.sh'
            }
        }
    }   
}