pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
  }
  environment {     
    DOCKERHUB_CREDENTIALS= credentials('dockerlogin')     
  }
  stages{
    stage('Build') {
      steps {
        sh 'docker-compose -f src/docker-compose.yml -f src/docker-compose.override.yml build'
        sh 'docker tag catalogapi:latest nmhieuit/catalogapi:latest'
      }
    }
    stage('push') {
      steps {
        sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
        echo 'Push Image Completed'
      }
    }
  }
}
