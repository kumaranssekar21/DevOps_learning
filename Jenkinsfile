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
							if (fileExists("${WORKSPACE}/DevOps_learning")) 
							{
								echo "Git Pull"
								bat 'git pull "https://github.com/kumaranssekar21/DevOps_learning.git"'
							}
							else
							{
								echo "Git Clone"
								bat 'git clone "https://github.com/kumaranssekar21/DevOps_learning.git"'
							}
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
