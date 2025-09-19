// Jenkinsfile en la raíz de tu repositorio
def notifySlack(String message) {
    // slackSend channel: '#devops', message: message
}

pipeline {
    agent any
    
    parameters {
        string(name: 'BRANCH', defaultValue: 'main', description: 'Branch to build')
        choice(name: 'DEPLOY_ENV', choices: ['dev', 'test', 'prod'], description: 'Deployment environment')
    }
    
    stages {
        stage('Checkout') {
            steps {
                git branch: params.BRANCH, 
                     url: 'https://github.com/tu-usuario/tu-repositorio.git',
                     credentialsId: 'github-credentials'
            }
        }
        
        // ... más stages
    }
}
