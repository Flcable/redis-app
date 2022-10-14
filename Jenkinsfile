pipeline {
    agent any

    stages {
        stage('build image docker'){
            steps{
                sh 'docker -t curso/app .' 
            }
        }
        stage('subir docker compose - redis e app'){
            steps {
                sh 'docker-compose up --build -d'
            }
        }
        stage('Sleep para subida de container'){
            steps {
                sh 'sleep 10'
            }
        }
        stage('teste aplicação'){
            steps {
                sh 'teste-app.sh'
            }
        }


    }
    
}