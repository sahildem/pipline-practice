pipeline {
  agent any
  tools {
    nodejs 'NodeJS 23'
  }
  environment {
    REPO_URL = 'https://github.com/sahildem/pipline-practice.git'
  }
  stages {
    stage('Clone Repository') {
      steps {
        git url: "${env.REPO_URL}", branch: 'main'
      }
    }
    stage('Install Dependencies') {
      steps {
        echo 'Installing node modules...'
        bat 'npm install'
      }
    }
    stage('Build App') {
      steps {
        echo 'Building the React app...'
        bat 'npm run build'
      }
    }
  }
}