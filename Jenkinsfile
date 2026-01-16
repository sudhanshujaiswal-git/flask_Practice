pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Installing Python dependencies'
                sh '''
                python3 -m venv venv
                . venv/bin/activate
                pip install -r requirements.txt
                '''
            }
        }

        stage('Test') {
            steps {
                echo 'Running unit tests'
                sh '''
                . venv/bin/activate
                pytest
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application to staging'
                sh '''
                echo "Application deployed successfully"
                '''
            }
        }
    }
}
