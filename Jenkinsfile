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
              sh 'pwd && ls && cd app'
              sh 'curl -L https://github.com/docker/compose/releases/download/1.29.2/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose'
              sh 'ls'
             sh 'docker-compose -f docker-compose.yml up -d'
            
          }
        }
    }  
}
