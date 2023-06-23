pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
  }
  stages{
    stage('Build') {
      steps { 
         withDockerRegistry([credentialsId: "dockerlogin", url: "src/Services/Catalog/Catalog.API"]) {
           script{
           app =  docker.build("asg")
           }
         }
      }
    }
  }
}
