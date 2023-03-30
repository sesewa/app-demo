pipeline {
    agent any

    
    stages {
        stage('Gitclone') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', credentialsId: 'ssh_git', url: 'https://github.com/sesewa/app-demo.git'
            }
        }
        stage('demo') {
          steps {
            echo 'Jenkins is working today'
             sh 'cd app'
             sh 'docker-compose . up -d'
            
          }
        }
    }  
}
