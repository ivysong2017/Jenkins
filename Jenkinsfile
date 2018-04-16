pipeline{
	agent any
	stages{
		stage('Example'){
			steps{
				sh 'echo "Hello World"'
			
				script{
					def browsers = ['chrome','firefox']
					//sh 'echo "browser size: ${browsers.size()}"'
					for(int i = 0; i < browsers.size(); ++i){
						sh 'echo "Testing the ${browsers[i]} browser"'
					}
				}
			}
		}
		
		stage('Branch Check'){
			steps{
				sh 'echo "start branch check....."'
				if(env.BRANCH_NAME == 'master'){
					sh 'echo "I am in the master branch".'
				}else{
					sh 'echo "I am in the branch ${env.BRANCH_NAME} "'
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
