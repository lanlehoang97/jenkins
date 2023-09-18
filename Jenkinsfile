pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git 'https://github.com/lanlehoang97/jenkins.git'
      }
    }

    stage('Build') {
      steps {
        withDockerRegistry(credentialsId: '4a7fd5f2-2d39-456d-8b1f-99893bae3f8c', url: 'https://index.docker.io/v1/') {
          sh 'docker build -t build-docker'
        }
      }
    }
  }
}
