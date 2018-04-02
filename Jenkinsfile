pipeline {
  agent {
    docker {
      image 'python:3.5.1'
    }
    
  }
  environment{
    DB_ENGINE = 'mysql'
  }
  stages {
    stage('build') {
      steps {
        sh 'python --version'
      }
    }
    stage('post') {
      steps {
        sh 'echo ${DB_ENGINE}'
        sh 'echo "hello, jenkins"'
      }
    }
  }
}
