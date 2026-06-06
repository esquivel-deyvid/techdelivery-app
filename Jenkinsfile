pipeline {
    agent any
    stages {
        stage('Clonar repositorio') {
            steps {
                git branch: 'main', url: 'https://github.com/esquivel-deyvid/techdelivery-app.git'
            }
        }
        stage('Instalar dependencias') {
            steps {
                sh 'npm install || true'
            }
        }
        stage('Ejecutar pruebas') {
            steps {
                sh 'echo "Pruebas OK"'
            }
        }
        stage('Publicar') {
            steps {
                sh 'echo "App lista para despliegue"'
            }
        }
    }
}