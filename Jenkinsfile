pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/suryakant1811/basic_cicd.git'
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
