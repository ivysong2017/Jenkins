pipeline {
  agent {
    docker {
      image 'python:3.5.1'
    }
    
  }
  stages {
    stage('build') {
      steps {
        sh 'python --version'
      }
    }
    stage('post') {
      steps {
        sh 'echo "hello, jenkins"'
      }
    }
  }
}
