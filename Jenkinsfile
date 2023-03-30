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
              sh 'pwd && ls'
              //sh 'cd /app'
              sh 'ls'
             sh 'docker-compose -f $WORKSPACE/app/docker-compose.yml up -d'
            
          }
        }
    }  
}
