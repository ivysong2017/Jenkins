pipeline{
	agent any
	stages{
		stage('Example'){
			echo 'Hello World'
			
			script{
				def browsers = ['chrome','firefox']
				for(int i = 0; i < browsers.size(); i++){
					echo "Testing the ${browsers[i]} browser"
				}
			}
		}
		
		stage('Build'){
			echo 'building phase....'
		}
	}
}
