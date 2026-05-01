pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/YOUR_USERNAME/YOUR_REPO.git'
            }
        }

        stage('Deploy to Nginx') {
            steps {
                sh '''
                    echo "Deploying HTML to Nginx..."
                    cp idx.html /var/www/html/index.html
                    sudo systemctl reload nginx
                    echo "Deployment completed."
                '''
            }
        }
    }
}
