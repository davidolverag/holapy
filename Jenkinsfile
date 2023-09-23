pipeline {
    agent any
    stages {
        stage('Ejecutar hola.py') {
            steps {
                script {
                    // Cambia la ruta al directorio donde se encuentra tu hola.py
                    def rutaHolaPy = "${WORKSPACE}/ruta/a/tu/hola.py"
                    
                    // Ejecuta el script Python
                    def resultado = bat(script: "python ${rutaHolaPy}", returnStatus: true)
                    
                    if (resultado == 0) {
                        echo 'Ejecución exitosa de hola.py'
                    } else {
                        error 'Error al ejecutar hola.py'
                    }
                }
            }
        }
    }
}
