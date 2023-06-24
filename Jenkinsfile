pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
  }
  stages{
    stage('Build') {
      steps {
        sh 'docker-compose -f src/docker-compose.yml -f src/docker-compose.override.yml build'
        sh 'docker tag catalogapi:latest nmhieuit/catalogapi:latest'
      }
    }
  }
}
