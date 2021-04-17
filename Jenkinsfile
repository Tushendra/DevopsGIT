
pipeline {
        agent {
            label 'master'
        }
        tools {
            maven 'java_maven'
            jdk 'java_home'
        }
    stages {
        stage ('Checkout the code') {
            steps{
                git branch: 'main', url: 'https://github.com/devopstrainers1/spring-petclinic.git'
            }
        }
        stage ('Code Compile') {
            steps{
                sh """
                mvn compile
                """
            }
        }
        stage ('JUNIT Test') {
            steps{
                sh """
                mvn test
                """
            }
        }
        stage ('Packaging') {
            steps {
                sh """
                mvn package
                """
            }
        }
      }   
}
