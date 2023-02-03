pipeline {
    agent any 
    stages {
        stage ('checkout code') {
            steps {
                sh 'git checkout'
            }
        }
        stage('deploy code to server') {
            steps {
                sh 'scp -i /var/lib/jenkins/key.pem -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/pipeline3/* centos@10.20.242.34:/var/www/html/'
                sh 'ssh -i /var/lib/jenkins/key.pem -o StrictHostKeyChecking=no service httpd restart'
            }
        }
    }
}
