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
							script{
								if (fileExists("${WORKSPACE}/test_file.txt"))
								{
									bat 'del "test_file.txt"'
								}
							}
							echo "Execute the Python file."
							bat "python Add_File.py"
					}
			}
			stage ("Archive Artifacts"){
				steps{
					archiveArtifacts artifacts: 'test_file.txt', fingerprint: true
				}
			}
				
			}
		
}
