pipeline {
    agent any

    environment {
      BRANCH_NAME = 'main'
      GIT_URL = 'https://github.com/yusuff0909/aws-cicd.git' 
    }

    stages {
      stage('git checkout') {
        steps{
            git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
        }
      }  
      stage('docker build') {
        steps{
            sh 'docker build -t aws-cicd .'
            sh 'docker images'
        }
      }
    }
}