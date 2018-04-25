pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''export M2_HOME=/opt/apache-maven-3.3.9 # your Mavan home path
'''
        sh '''export PATH=$PATH:$M2_HOME/bin
'''
        sh 'mvn --version'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }
    stage('Deliver') {
      steps {
        sh './jenkins/scripts/deliver.sh'
      }
    }
  }
}