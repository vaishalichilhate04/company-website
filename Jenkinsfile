pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Deploy to Apache') {
            steps {
                sh '''
                    sudo cp index.html /var/www/html/index.html
                    sudo systemctl restart httpd
                '''
            }
        }
    }
}
