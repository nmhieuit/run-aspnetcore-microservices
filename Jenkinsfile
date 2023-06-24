pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
  }
  stages{
    stage('Build') {
      steps { 
        sh 'sh docker-compose -f docker-compose.yml -f docker-compose.override.yml build'
        sh 'docker tag catalogapi:latest nmhieuit/catalogapi:latest'
      }
    }
  }
}
