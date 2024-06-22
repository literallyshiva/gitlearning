pipeline {
    agent any
    stages {
        stage('Welcome') {
            steps {
                echo 'Hi, You are inside the pipeline'
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
    }
    post {
        success {
            emailext(
                body: 'Hi, the latest build on your project is successful',
                subject: 'Build notification',
                to: 'shivanandt120@gmail.com'
            )
        }
    }
}

