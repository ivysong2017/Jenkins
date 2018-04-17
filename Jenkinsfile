pipeline {
  agent any
  environment{
    DB_ENGINE = 'mysql'
    DBPASSWORD=credentials('DB_PASSWORD')
  }
  stages {
    stage('Build') {
      steps {
        sh 'echo "Build...."'
        script{
          echo "db password: ${env.DBPASSWORD}"
        }
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
