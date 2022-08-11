pipeline{

agent any

tools{
maven 'maven3.8.2'

}

stages{

  stage('CheckOutCode'){
    steps{
    git credentialsId: '9e632459-f64d-4380-8586-e853eb946bad', url: 'https://github.com/Chakriwipro/maven-web-application.git'
	
    }
  }
  
  stage('Build'){
  steps{
  sh  "mvn clean package"
  }
  }

 stage('Execute SonarQubeReport'){
  steps{
  sh  "mvn clean sonar:sonar"
       }
     }
  }
}
