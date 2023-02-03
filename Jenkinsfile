pipeline {
    agent any 
    stages {
        stage ('checkout code') {
            steps {
                sh 'git checkout'
            }
        }
        stage('Deploy in production') {
            steps {
                echo "deployed to production"
            }
        }
    }
}
