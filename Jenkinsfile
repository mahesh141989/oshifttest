#!/bin/usr/env groovy
pipeline {
  agent any
  stages {
    stage('build') {
      sh 'mvn clean package'
    }
    post {
      success {
        echo "Now archiving"
        archiveArtifacts artifacts: '**/target/*.war'
      }
    }
  }
}
