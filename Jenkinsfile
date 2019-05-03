pipeline {
  agent any
  stages {
    stage('Install Testcafe') {
      steps {
        sh 'npm install testcafe testcafe-reporter-xunit'
      }
    }
    stage('Run TestCafe') {
      steps {
        sh 'node_modules/.bin/testcafe chrome tests/**/* -r xunit:res.xml'
      }
    }
  }
}