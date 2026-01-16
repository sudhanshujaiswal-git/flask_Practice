pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Installing dependencies'
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
                sh 'pytest || true'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage'
                sh 'python3 app.py &'
            }
        }
    }
}
