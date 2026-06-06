pipeline {
    agent {
        docker {
            image 'node:18'
            reuseNode true
        }
    }
    stages {
        stage('Clonar repositorio') {
            steps {
                git branch: 'main', url: 'https://github.com/esquivel-deyvid/techdelivery-app.git'
            }
        }
        stage('Instalar dependencias') {
            steps {
                sh 'npm install'
            }
        }
        stage('Ejecutar pruebas') {
            steps {
                sh 'npm test'
            }
        }
        stage('Publicar') {
            steps {
                sh 'echo "App lista para despliegue"'
            }
        }
    }
}