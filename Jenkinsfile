#!groovy
  def app
pipeline {

 agent any 
  stages {
    
     stage('Checkout'){    
       steps {
          sh "git checkout ${env.BRANCH_NAME}"               
       }
     }
     stage('Sonar') {
            steps {
               sh "whoami"
               //sh "mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.3.0.603:sonar -Dsonar.host.url=http://sonar-devel.local"
            }
        }  
    
    stage('Create Docker Image') {
     steps{
      //sh "sudo docker stop devops-poc/pipeline:latest" 
      //sh "sudo docker rm devops-poc/pipeline:latest" 
      sh "sudo docker-compose up -d"
          }
     }
 
    
    

  }
}