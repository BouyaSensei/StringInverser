pipeline{
  agent any

  stages {
   stage('build'){
    steps {
      script {
      if(isUnix(){
        sh 'make'
       stage('Permissions'){
        steps{
          script{
            sh 'chmod'
          }
        }
       }
       stage('Nettoyage'){
          sh 'make clean'
       }
       } else {
        bat 'make'
         stage('Nettoyage'){
          bat 'make clean'
       }
      }
        
     }
    }
   }
  }
  
  
 }
}
