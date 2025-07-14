pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t my-app:latest .'
      }
    }
    stage('Test') {
      steps {
        sh 'npm test'  // or pytest, maven test, etc.
      }
    }
    stage('Deploy') {
      steps {
        sh 'kubectl apply -f k8s/deployment.yaml'
      }
    }
  }
}

