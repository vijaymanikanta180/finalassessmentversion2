pipeline {
    agent { 
       label 'docker'
    }
  
    stages {
        stage('pull git code') {
            steps { 
                git branch: 'main',
                credentialsId: 'vijaymanikanta180',
                url: 'https://github.com/vijaymanikanta180/finalassessmentversion2.git' 
            } 
        }
       
        stage('Build docker') {
            steps {
                // Run docker
                sh "docker build -t apache2:2.0 ."
                sh "docker run -itd -p 80:80 apache2:2.0"                
            }
        }
    }
}
