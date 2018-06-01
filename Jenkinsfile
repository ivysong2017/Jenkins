pipeline {
  agent{
    dockerfile{
      //the -v argument is to make docker inside docker container have enough privilege to run
      args '-u root:root -v "/var/run/docker.sock:/var/run/docker.sock:rw"'
    }
  }
  environment{
    DB_ENGINE = 'mysql'
    DBPASSWORD=credentials('DB_PASSWORD')
  }
  stages {
    stage('Build') {
      steps {
        sh 'echo "Build...."'
        script{
          //echo "db password: ${env.DBPASSWORD}"
          sh '''
          cd /home/jenkins/onboardingui
          bash -x downloadsrccode.sh
          '''
        }
      }
    }
    stage('Test'){
      steps {
        sh 'echo "Test...."'
        script{
          withCredentials([string(credentialsId:"DB_PASSWORD", variable:"DBPASSWD")]){
            echo "db passwd: ${DBPASSWD}"
          }
          
          sh '''
          cd /home/jenkins/onboardingui
          docker build -f SeleniumTestDockerfile .
          '''
        }
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo ${DB_ENGINE}'
        sh 'echo "Deploy...."'
      }
    }
    
  }
  post{
    always{
      junit '/home/jenkins/onboardingui/onboardingsrc/*.xml'
    }
  }
}
