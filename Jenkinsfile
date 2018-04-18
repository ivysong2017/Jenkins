pipeline {
  agent any
  environment{
    DB_ENGINE = 'mysql'
  }
  stages {
    stage('Back-end') {
      agent {
        docker { image 'maven:3-alpine' }
      }
      steps {
        //sh 'python --version'
        sh 'echo "Back-end..."'
        sh 'mvn --version'
      }
    }
    stage('Front-end'){
      agent {
        docker { image 'node:7-alpine' }
      }
      steps {
        sh 'echo "Front-end..."'
        sh 'node --version'
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
