pipeline {
   agent any
   tools{
       maven 'M2_HOME'
       }

   stages {
	stage('Print') {
        steps {
		Echo 'Hello every One'
               }
            }
	stage('Checkout') {
        steps {
		git 'https://github.com/devopscbabu/maven-sample.git'
               }
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
         }         
      }
