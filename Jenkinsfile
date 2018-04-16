pipeline{
	agent any
	stages{
		stage('Example'){
			sh 'echo "Hello World"'
			
			script{
				def browsers = ['chrome','firefox']
				for(int i = 0; i < browsers.size(); i++){
					sh 'echo "Testing the ${browsers[i]} browser"'
				}
			}
		}
		
		stage('Build'){
			sh 'echo "building phase...."'
		}
	}
}
