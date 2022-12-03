pipeline {
    agent any

    stages {
        stage('Fetch code') {
            steps {
                 git branch: 'main', poll: false, url: 'https://github.com/Narendra-sin/CICDTEST.git'
            }
        }
        stage('Install and Configure Apache') {
            steps {
                sh 'sudo apt install apache2 -y'
            }
        }
        stage('Deploy application') {
            steps {
                sh 'sudo cp -R * /var/www/html/'
            }
        }

    }
  
}
