pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
  }
  stages{
    stage('Build') { 
      steps { 
       withDockerRegistry([credentialsId: "dockerlogin", url: ""]) {
         script{
           app =  docker.build("nmhieuit")
         }
       }
      }
    }
  }
}
