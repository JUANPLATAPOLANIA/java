pipeline {
    agent { label 'agent1' }  // Aquí especificas el nombre del agente

    stages {
        // Stage de descarga del código
        stage('Descargar Código') {
            steps {
                git 'https://github.com/JUANPLATAPOLANIA/java.git'
            }
        }

        // Stage de build (compilación) para Java
        stage('Build') {
            steps {
                script {
                    sh './mvnw clean install'  // Usando Maven para construir el proyecto
                }
            }
        }

        // Stage de ejecución de pruebas
        stage('Pruebas') {
            steps {
                script {
                    sh './mvnw test'  // Usando Maven para ejecutar las pruebas
                }
            }
        }
    }
}
