pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
                // Copy your HTML files to /var/www/html
                sh 'sudo cp -r index.html /usr/share/nginx/html/'
            }
        }
    }

    post {
        success {
            echo 'Deployment successful'
        }
    }
}
