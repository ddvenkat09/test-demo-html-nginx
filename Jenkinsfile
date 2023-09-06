pipeline {
    agent any

    stages {
        stage('Deploy to /var/www/html') {
            steps {
                // Copy your HTML files to /var/www/html
                sh 'cp -r index.html /usr/share/nginx/html/'
                sh 'service nginx restart'
            }
        }
    }

    post {
        success {
            echo 'Deployment successful'
        }
    }
}
