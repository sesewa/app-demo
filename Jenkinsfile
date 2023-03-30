pipeline {
    agent any

    
    stages {
        stage('Gitclone') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', credentialsId: 'ssh_git', url: 'https://github.com/sesewa/app-demo.git'
            }
        }
        stage('NPM Install') {
          steps {
            echo 'Jenkins is working'
            
          }
        }
    }  
}
