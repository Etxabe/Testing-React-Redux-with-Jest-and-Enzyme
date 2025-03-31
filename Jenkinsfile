pipeline {
    agent any

    stages {
        // Etapa de Checkout (clona el repositorio)
        stage('Checkout') {
            steps {
                git branch: 'main', credentialsId: 'tu-credencial-id', url: 'https://github.com/Etxabe/Testing-React-Redux-with-Jest-and-Enzyme.git'
            }
        }

        // Etapa de Instalación de dependencias
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        // Etapa de Construcción de la aplicación
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        // Etapa de Ejecución de pruebas (si las tienes configuradas)
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        // Etapa de Despliegue (puedes añadir el despliegue aquí)
        stage('Deploy') {
            steps {
                echo 'Desplegando la aplicación...'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finalizado'
        }
    }
}
