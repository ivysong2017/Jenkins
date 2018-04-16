pipeline{
	agent any
	stages{
		stage('Example'){
			steps{
				sh 'echo "Hello World"'
			
				script{
					def browsers = ['chrome','firefox']
					for(int i = 0; i < browsers.size(); ++i){
						sh 'echo "Testing the ${browsers[i]} browser"'
					}
				}
			}
		}
		
		stage('Build'){
			steps{
				sh 'echo "building phase...."'
			}
		}
	}
}
