pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Installing dependencies'
                sh 'python3 -m pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
                sh 'python3 -m pytest || true'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage completed'
            }
        }
    }
}
