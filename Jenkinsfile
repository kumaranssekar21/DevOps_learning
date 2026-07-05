pipeline{
	agent any
	environment{
			REPO_URL = "https://github.com/kumaranssekar21/DevOps_learning.git"
			REPO_BRANCH = "main"
			REPO_DIR = "${WORKSPACE}"
			
		}
		stages{
			stage("Cloning"){
					steps{
						echo "Git Cloning"
						bat 'git clone "https://github.com/kumaranssekar21/DevOps_learning.git"' 
					
						 }
				}
				
			}
		
}
