pipeline {
    agent any

    stages {
        stage('Deploy to /var/www/html') {
            steps {
                // Copy your HTML files to /var/www/html
                sh 'sudo cp -r index.html /usr/share/nginx/html/'
                sh 'sudo service nginx restart'
            }
        }
    }

    post {
        success {
            echo 'Deployment successful'
        }
    }
}
