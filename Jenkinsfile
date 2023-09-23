pipeline {
    agent any

    stages {
        stage('Ejecutar Contenedor Docker') {
            steps {
                // Ejecutar el contenedor Docker
                sh 'docker run mi-app:latest python hola.py'
            }
        }
    }

    post {
        always {
            // Limpiar el contenedor Docker después de la ejecución
            sh 'docker rm -f $(docker ps -a -q)'
        }
    }
}
