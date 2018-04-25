pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'export M2_HOME=/Applications/apache-maven-3.5.3'
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