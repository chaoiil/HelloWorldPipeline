pipeline {
    agent any

    stages {
        stage('Setup') {
            steps {
                echo 'Configuration environnement...'
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Build') {
            steps {
                echo 'Build du projet...'
                sh 'python hello_world.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Execution des tests...'
                sh 'pytest tests/'

            }
        }
    }

    post {
        always {
            echo 'Terminé...''
        }
    }
}