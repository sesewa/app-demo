pipeline {
    agent any

    
    stages {
//         stage('Gitclone') {
//             steps {
//                 // Get some code from a GitHub repository
//                 git branch: 'main', credentialsId: 'ssh_git', url: 'https://github.com/sesewa/app-demo.git'
//             }
//         }
        stage('demo') {
          environment { 
                SSH_CRED = credentials('sesewa-devops')
            }
          steps {
            script {
                    sh """
                    #!/bin/bash
                    ssh -i "$SSH_CRED" -o StrictHostKeyChecking=no ubuntu@ec2-35-182-203-76.ca-central-1.compute.amazonaws.com << EOF
                    #git clone https://github.com/sesewa/app-demo.git
                    pwd
                    cd app-demo/app
                    docker-compose -f docker-compose.yml up -d
                    exit
                    EOF
                    """
                }
            
          }
        }
    }  
}
