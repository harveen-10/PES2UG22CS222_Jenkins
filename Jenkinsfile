pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Starting Build Stage'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Tests'
                sh './hello || exit 1'  
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo Deploying hello.cpp output'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'  
        }
        failure {
            echo 'Pipeline failed! Check logs for errors.'
        }
    }
}
