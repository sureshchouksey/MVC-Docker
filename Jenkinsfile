#!groovy
  def app
pipeline {

 agent any 
  stages {
    
     stage('Checkout code') {
        steps {
            checkout scm
        }
    }
    
    stage('Create Docker Image') {
     steps{
			sh "docker-compose up -d"
          }
     }
 
    
    

  }
}