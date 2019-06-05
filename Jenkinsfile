#!/bin/usr/env groovy
pipeline {
  agent any
  stages {
    stage('buid'){
      steps {
        sh 'mvn clean package'
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
