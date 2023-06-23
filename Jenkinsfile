pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
  }
  stages{
    stage('Build') { 
      steps { 
        app = docker.build('-f src/Services/Catalog/Catalog.API);     
        sh 'docker tag catalogapi:latest nmhieuit/catalogapi:latest'
      }
    }
  }
}
