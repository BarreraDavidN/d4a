pipeline{
	agent any
	stages{
		stage('Initial Setup'){
			steps{
				sh 'echo Starting...'
			}
		}
	
		stage('Checking Docker'){
			steps{
				sh 'sudo docker ps'
			}
		}
	}

}
