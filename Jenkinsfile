pipeline {
  agent any
  stages {
    stage('Cloning Git') {
      steps {
        git([url: 'https://github.com/ngokulsathish/docker.git', branch: 'master'])
 	checkout scm

      }
    }
    stage('Building image') {
      steps{
     
      sh "sudo docker build -t image:v1 ."


          }
      }
   
    
    
  }
}
