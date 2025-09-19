pipeline {
    agent any
    
    stages {
        stage('Execute on test server') {
            steps {
                script {
                    def server = [name: 'test', ip: '34.95.199.71']
                    def usuario = 'jenkins'
                    def sshKey = '/home/jenkins/.ssh/id_rsa'
                    
                    sh """
                        ssh -i ${sshKey} \\
                        -o StrictHostKeyChecking=no \\
                        ${usuario}@${server.ip} \\
                        '. /home/gitlabops/testgithub/test-git.sh'
                    """
                }
            }
        }
    }
}
