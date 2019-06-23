#!/bin/usr/env groovy
pipeline {
  agent any
  tools { 
        maven 'default'  
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
