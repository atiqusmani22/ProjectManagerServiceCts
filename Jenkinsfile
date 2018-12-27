pipeline{

	agent{
		docker 
		{
			image 'java:8'
			
		
		}
	}
	environment
	{
		CI = 'true'
	}
	stages{
		stage('Build'){
			steps{
				echo 'Building......'
				withMaven() {
		            git "https://github.com/atiqusmani22/ProjectManagerService"
		            sh './mvnw install dockerfile:build'
		        }
				
			}
		}
		stage('Test'){
			steps{
				echo 'Testing......'
			}
		}
	
	}

}