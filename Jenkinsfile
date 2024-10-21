pipeline {
    agent any

    stages {
        stage('Configuration') {
            steps {
                echo 'Configuration de l'environnement...'
                sh 'pip install -r requirements.txt' 
            }
        }

        stage('Compilation') {
            steps {
                echo 'Compilation du projet...'
                sh 'python hello_world.py'
            }
        }

        stage('Tests') {
            steps {
                echo 'Exécution des tests...'
                sh 'pytest tests/'
            }
        }
    }

    post {
        always {
            echo 'Nettoyage...'
        }
    }
}
