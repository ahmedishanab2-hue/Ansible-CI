
pipeline {
    agent any

    stages {
        stage('Install Nginx') {
            steps {
                sh 'ansible-playbook -i localhost, -c local install-nginx.yml'
            }
        }
    }

    post {
        success {
            echo 'Nginx deployment completed successfully.'
        }
        failure {
            echo 'Nginx deployment failed. Check the console output.'
        }
        always {
            echo 'Pipeline execution finished.'
        }
    }
}