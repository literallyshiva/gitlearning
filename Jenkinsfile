pipeline {
    agent any
    stages {
        stage('welcome') {
            steps {
                echo 'poda'
            }
        }
        stage('build') {
            steps {
                echo 'skipping build'
            }
        }
        stage('test') {
            steps {
                echo 'skipping test'
            }
        }
        stage('deploy') {
            steps {
                script {
                    // Running apt-get update and installing nginx
                    sh '''
                    echo "${sudoPassword}" | sudo -S apt-get update
                    echo "${sudoPassword}" | sudo -S apt-get install -y nginx
                    '''
                    
                    // Copying index.html to nginx directory
                    sh '''
                    echo "${sudoPassword}" | sudo -S cp index.html /var/www/html/
                    '''

                    // Restarting nginx service
                    sh '''
                    echo "${sudoPassword}" | sudo -S systemctl restart nginx
                    '''
                }
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}
