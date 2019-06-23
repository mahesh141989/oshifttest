#!/bin/usr/env groovy
pipeline {
  agent any
  tools { 
        maven 'Maven 3.3.9'  
    }
  stages {
    stage('buid'){
      steps {
        bat 'mvn clean install package'
      }
      post {
        success {
          echo "Now Archiving"
          archiveArtifacts artifacts: '**/target/*.war'
        }
      }
    }
  }
}
