pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
                // Copy your HTML files to /var/www/html
                sh 'sudo cp -r index.html /var/www/html'
            }
        }
    }

    post {
        success {
            // Clean up workspace and temporary files
            cleanWs()
        }
    }
}
