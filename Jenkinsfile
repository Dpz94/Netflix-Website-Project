pipeline {
    agent any 
    stages {
        stage ('checkout code') {
            steps {
                git checkout
            }
        }
        stage('deploy code to server') {
            sh 'scp -i /var/lib/jenkins/key.pem -o StrictHostKeyChecking=no * centos@10.20.242.34:/var/www/html'
            sh 'ssh -i /var/lib/jenkins/key.pem -o StrictHostKeyChecking=no service httpd restart'
        }
    }
}
