pipeline {
   agent any
   tools{
       maven 'M2_HOME'
       }

   stages {
	stage('Checkout') {
        steps {
		https://github.com/yeswanthsai2005/maven-sample.git
            }
      stage('Build my job') {
        steps {
            sh 'mvn clean compile'
               }
            }
      stage('Package you App') {
         steps{
             sh 'mvn clean package'
               }
            }
      stage('Sonar Checks') {
	 steps{
	    withSonarQubeEnv(credentialsId: 'Jenkins-sonar-token', installationName: 'Sonarcloud') {
    	    sh 'mvn clean package sonar:sonar'
     		}
  	 }
      } 
   }         
}
