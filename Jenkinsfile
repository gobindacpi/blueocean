pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''date
pwd'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test step'
          }
        }

        stage('test per') {
          steps {
            echo 'test per'
          }
        }

      }
    }

    stage('deploy') {
      parallel {
        stage('deploy') {
          steps {
            echo 'deployment done'
          }
        }

        stage('sleep') {
          steps {
            sleep 15
          }
        }

      }
    }

  }
}