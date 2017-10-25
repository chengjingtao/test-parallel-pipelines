pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        sh 'echo clone'
      }
    }
    stage('Build') {
      steps {
        parallel(
          "Build": {
            sh 'echo build'
            input 'will build ?'
            
          },
          "Scan": {
            sh 'echo scan'
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
        sh 'echo test'
      }
    }
    stage('deploy') {
      steps {
        sh 'echo deploy'
      }
    }
  }
}