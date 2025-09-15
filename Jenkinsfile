pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Properly clone the Git repo
                git branch: 'main', url: 'https://github.com/ermin700/my-jenkins-pipeline.git'
            }
        }

        stage('Verify') {
            steps {
                echo "Repository cloned successfully!"
                sh 'ls -la'  // Verify files
            }
        }
    }
}
