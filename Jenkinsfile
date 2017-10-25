pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        sh 'sh "echo clone"'
      }
    }
    stage('Build') {
      steps {
        parallel(
          "Build": {
            sh 'sh "echo build"'
            input 'will build ?'
            
          },
          "Scan": {
            sh 'sh "scan"'
            input 'will scan'
            
          },
          "GodMod": {
            input 'God coming?'
            
          }
        )
      }
    }
    stage('Test') {
      steps {
        sh 'sh "echo test"'
      }
    }
    stage('deploy') {
      steps {
        sh 'sh "echo deploy"'
      }
    }
  }
}