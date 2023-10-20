pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        echo 'helloword'
      }
    }

    stage('stage2') {
      parallel {
        stage('stage2') {
          steps {
            echo 'hello'
          }
        }

        stage('stage2.1') {
          steps {
            sh '''date
ls -l
pwd
whoami'''
          }
        }

      }
    }

    stage('stage3') {
      steps {
        sleep 300
      }
    }

  }
}