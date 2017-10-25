pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        sh 'echo clone'
      }
    }
    stage('Build') {
        failFast true
        parallel {
            stage('Branch A') {
                steps {
                    echo "On Branch A"
                    input "Branch A OK ?"                    
                }
            }
            stage('Branch B') {
                steps {
                    echo "On Branch B"
                    input "Branch B OK ?"
                }
            }
            stage('Branch C') {
                steps {
                    echo "On Branch C"
                    input "Branch C OK ?"
                }
            }
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