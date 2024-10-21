pipeline {
    agent any

    stages {
        stage('Configuration') {
            steps {
                echo 'Configuration de l'environnement...'
                sh 'pip install -r requirements.txt' // Pour Python
                // sh 'mvn clean install' // Pour Java (Maven)
                // sh 'npm install' // Pour Node.js
            }
        }

        stage('Compilation') {
            steps {
                echo 'Compilation du projet...'
                sh 'python hello_world.py' // Pour Python
                // sh 'javac HelloWorld.java && java HelloWorld' // Pour Java
                // sh 'node hello_world.js' // Pour Node.js
            }
        }

        stage('Tests') {
            steps {
                echo 'Exécution des tests...'
                sh 'pytest tests/' // Pour Python
                // sh 'mvn test' // Pour Java
                // sh 'npm test' // Pour Node.js
            }
        }
    }

    post {
        always {
            echo 'Nettoyage...'
        }
    }
}
