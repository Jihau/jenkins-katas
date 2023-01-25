pipeline {
  agent any
  stages {
    stage('Parallel execution') {
      parallel {
        stage('Say hello') {
          steps {
            sh 'echo "hello world"'
          }
        }

        stage('error') {
          agent {
            docker {
              image 'python:latest'
            }

          }
          steps {
            sh 'echo moi'
          }
        }

      }
    }

  }
}