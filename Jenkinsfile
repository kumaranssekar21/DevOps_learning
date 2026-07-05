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
						script {
							if [-d  "DevOps_learning"] then
							echo "Git Pull"
							bat 'git pull "https://github.com/kumaranssekar21/DevOps_learning.git"' 
							
						}
						
					
						 }
				}
			stage ("Build")
			{
					steps{
							echo "Execute the Python file."
							bat "python Add_File.py"
					}
			}
				
			}
		
}
