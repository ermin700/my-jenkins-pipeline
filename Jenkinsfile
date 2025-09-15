pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository from GitHub
                git branch: 'main', url: 'https://github.com/ermin700/my-jenkins-pipeline.git'
            }
        }

        stage('Verify') {
            steps {
                // Simple verification step
                echo "Repository cloned successfully!"
                sh 'ls -la'  // List files in the workspace
            }
        }
    }

    post {
        success {
            echo "Pipeline completed successfully!"
        }
        failure {
            echo "Pipeline failed. Check the logs for details."
        }
    }
}


