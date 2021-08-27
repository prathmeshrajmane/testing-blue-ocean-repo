pipeline {
  agent none
  stages {
    stage('Maven Install') {
      agent {
        docker {
          image 'maven:3.5.0'
        }

      }
      steps {
        sh 'echo "hello"'
      }
    }

    stage('Docker Build') {
      agent any
      steps {
        sh 'docker build -t simple-nginx .'
      }
    }

  }
}