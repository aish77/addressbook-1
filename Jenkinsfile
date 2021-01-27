pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'running the build'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'testing the app'
          }
        }

        stage('testing for multiple environments') {
          steps {
            echo 'testing for dev and test'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying the app'
        cleanWs(cleanWhenFailure: true)
      }
    }

  }
}