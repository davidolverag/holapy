pipeline {
  agent any
  stages {
    stage('Ejecutar Contenedor Docker') {
      steps {
        sh 'docker run mi-app:latest python hola.py'
      }
    }

  }
}