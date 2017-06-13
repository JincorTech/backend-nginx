pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build . -t backend-nginx:latest'
      }
    }
    stage('Deploy') {
      steps {
        sh 'docker tag backend-nginx registry.jincor.com/backend/nginx:latest'
        sh 'docker push registry.jincor.com/backend/nginx:latest'
      }
    }
  }
}