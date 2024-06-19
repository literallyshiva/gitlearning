pipeline {
    agent any
    stages {
        stage('Welcome') {
            steps {
                echo 'Hi , You are inside the pipeline'
            }
        }
        // stage('Checkout') {
        //     steps {
        //         git 'https://github.com/AnandLoganathan/jenkinspipeline.git'
        //     } 
        // }
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
