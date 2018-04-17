pipeline {
  agent any
  environment{
    DB_ENGINE = 'mysql'
  }
  stages {
    stage('Build') {
      steps {
        sh 'echo "Build...."'
      }
    }
    stage('Test'){
      steps {
        sh 'echo "Test...."'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo ${DB_ENGINE}'
        sh 'echo "Deploy...."'
      }
    }
  }
}
