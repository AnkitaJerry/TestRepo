pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        sh 'echo'
        bat 'echo code >1.txt'
      }
    }
    stage('UnitTest') {
      parallel {
        stage('UnitTest') {
          steps {
            bat 'echo Unit Test > 2.txt'
          }
        }
        stage('UITest') {
          steps {
            bat 'echo uitest > 3.txt'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        bat 'echo deploy test > 4.txt'
      }
    }
  }
}