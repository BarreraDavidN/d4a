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
                                sh 'COPY https://github.com/BarreraDavidN/d4a/blob/master/Dockerfile /var/jenkins_home/workspace/Pipeline EDSI'
								sh 'COPY https://github.com/BarreraDavidN/d4a/blob/master/index.php /var/jenkins_home/workspace/Pipeline EDSI'
								sh 'COPY https://github.com/BarreraDavidN/d4a/blob/master/db.php /var/jenkins_home/workspace/Pipeline EDSI'
								sh 'sudo docker build --tag="php54" .'
								
                        }
						
                }
				
				stage('Deploy Container'){
                        steps{
                                sh 'COPY https://github.com/BarreraDavidN/d4a/blob/master/docker-compose.yml /var/jenkins_home/workspace/Pipeline EDSI'
								sh 'docker-compose up -d'
                        }
						
                }
        }

}
