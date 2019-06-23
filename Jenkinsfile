#!/bin/usr/env groovy
pipeline {
  agent window_node
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
