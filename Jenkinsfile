pipeline{
	agent any
	environment{
		DB_ENGINE = 'my sql'
		DISABLE_AUTH = 'true'
	}
	stages{
		stage('Example'){
			steps{
				sh 'echo "Hello World"'
			
				script{
					def browsers = ['chrome','firefox']
					//sh 'echo "browser size: ${browsers.size()}"'
					for(int i = 0; i < browsers.size(); ++i){
						echo "Testing the ${browsers[i]} browser"
					}
				}
			}
		}
		
		stage('Branch Check'){
			steps{
				sh 'echo "start branch check....."'
				sh 'printenv'
				
				script{
					if(env.BRANCH_NAME == 'master'){
						echo "I am in the master branch"
					}else{
						echo "I am in the branch ${env.BRANCH_NAME} "
					}
				}
				//sh 'echo "building phase...."'
			}
		}
		
		stage('Build'){
			steps{
				sh 'echo "building phase...."'
			}
		}
	}
}
