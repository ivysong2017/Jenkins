pipeline {
  //agent {
    //docker {
      //image 'python:3.5.1'
    //}
    
  //}
  environment{
    DB_ENGINE = 'mysql'
  }
  stages {
    stage('build') {
      steps {
        //sh 'python --version'
        sh 'echo "build...."'
      }
    }
    stage('check'){
      steps {
        input "Does the staging environment look ok?"
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
