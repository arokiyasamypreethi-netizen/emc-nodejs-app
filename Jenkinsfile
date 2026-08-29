pipeline {
  agent any

  environment {
    IMAGE_NAME = 'emc-nodejs-app:latest'
     DOCKER_HOST = 'tcp://localhost:2375'
  }

  stages {
    stage('Checkout Code') {
      steps {
        git branch: 'main', url: 'https://github.com/Venkiemc/emc-nodejs-app.git'
      }
    }
    stage('Build Docker Image') {
      steps {
        bat '"C:\\Users\\hp\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" build -t %IMAGE_NAME% .'
      }
    }

    stage('Show Docker Images') {
      steps {
        bat  '"C:\\Users\\hp\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" images'
      }
    }
  }
}
