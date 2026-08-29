pipeline {
    agent any
    environment {
        IMAGE_NAME = 'emc-nodejs-app:latest'
        DOCKER_HOST = 'tcp://localhost:2375'
    }
    stages {
        stage('Code Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/arokiyasamypreethi-netizen/emc-nodejs-app.git'
            }
        }
        stage('Images Build') {
            steps {
               // Make sure there is NO raw 'docker build' word at the front here
               bat '"C:\\Users\\hp\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" build -t %IMAGE_NAME% .'
            }
        } 
        stage('Images List') {
            steps {
               // Make sure there is NO raw 'docker images' word at the front here
               bat '"C:\\Users\\hp\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" images'
            }
        } 
    }
}
