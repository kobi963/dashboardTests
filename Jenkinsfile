pipeline {
  agent any
  stages {
    stage('build') {
      steps {
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