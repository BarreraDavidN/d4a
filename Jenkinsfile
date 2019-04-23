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

                stage('Build Docker Image'){
                        steps{
                                sh 'cd /home/backup/php54'
								sh 'sudo docker build --tag="php54" .'
								sh 'sudo docker run -p 80:80 --name phpedsi --rm php54'
                        }
						
                }
				
				stage('Deploy Container'){
                        steps{
                                sh 'cd /home/backup/d4a'
								sh 'docker-compose up -d'
                        }
						
                }
        }

}
