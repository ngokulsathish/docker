pipeline {
    
  agent any
  stages {
    stage('Cloning Git') {
      steps {
        git([url: 'https://github.com/umeshbalajishankaraws/docker', branch: 'master'])
        
      }
    }
    stage('Building image') {
      steps{
     
      sh "sudo docker build -t nginx_custom:v1 ."
          }
      }
    stage('List image') {
      steps{
     
      sh "sudo docker images"
          }
      }
    stage('Create a container from the image') {
      steps{
     
      sh "sudo docker run -td --name nginx --publish 8081:80 nginx_custom:v1"
          }
      }
  }
}
