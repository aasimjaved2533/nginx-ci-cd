pipeline{
    agent any

    stages {
        stage('clone code') {
            steps {
                git'https://github.com/aasimjaved2533/nginx-ci-cd.git'
            }
        }

        stage('Deploy code') {
            steps {
                sh '''
                    sudo cp -r * /var/www/html/
                    sudo systemctl restart nginx
                '''
            }
        }
    }
}
