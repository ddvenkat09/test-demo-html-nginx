pipeline {
    agent any

    stages {
        stage('Deploy to /var/www/html') {
            steps {
                // Copy your HTML files to /var/www/html
                sh 'sudo cp -r * /var/www/html/'

                // Ensure proper permissions (optional)
                sh 'sudo chown -R www-data:www-data /var/www/html/'

                // Restart Nginx to apply changes
                sh 'sudo systemctl restart nginx'
            }
        }
    }

    post {
        success {
            echo 'Deployment successful'
        }
    }
}
