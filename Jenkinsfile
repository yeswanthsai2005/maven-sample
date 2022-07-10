pipeline {
    agent any
    tools {
       maven 'maven 3.8.6'
    }
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                echo 'hi'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package  -DskipTests'
            }
        }
        stage('sonarqube checks') {
            steps {
                script {
                withSonarQubeEnv(installationName: 'sonarqube-2', credentialsId: 'NewSonarToken2') {
                 sh 'mvn clean package sonar:sonar'
                 }
                 
            }
        }
    }
}
}
