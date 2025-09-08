pipeline {
    agent any

    stages {
        stage('1. Clonar Código') {
            steps {
                echo 'Obteniendo el código más reciente desde GitHub...'
                // ▼▼▼ ¡¡IMPORTANTE!! Cambia esta URL por la de tu repositorio ▼▼▼
                git url: 'https://github.com/TU_USUARIO_DE_GITHUB/tu-repositorio.git', branch: 'main'
            }
        }
        stage('2. Desplegar en Servidor Web') {
            steps {
                echo 'Copiando archivos al servidor Nginx...'
                // Este comando copia el html a la carpeta compartida
                sh 'cp -f *.html /var/website-data/'
            }
        }
    }
    post {
        success {
            echo '¡Sitio web actualizado con éxito! ✅'
        }
    }
}
