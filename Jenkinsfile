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
                sh 'sudo apt-get update && sudo apt-get install -y nginx'
                sh 'sudo cp index.html /var/www/html/'
                sh 'sudo systemctl restart nginx'
            }
        }
    }
}
