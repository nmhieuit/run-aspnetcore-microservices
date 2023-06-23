pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
  }
  stages{
    stage('Build') { 
      steps { 
        sh 'docker-compose -f docker-compose.yml -f docker-compose.override.yml build'     
        echo 'Docker-compose-build Build Image Completed'       
      }
    }
  }
}
