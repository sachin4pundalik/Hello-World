pipeline{
	agent any
		stages{

			stage('One'){
				steps{
					echo 'Hi, this Sachin..'
				}	
			 }

			stage('Two'){
				steps{
					input('Do you want to proceed ?')
				}	
			 }

			 stage('Three'){

				when {
					not {
					  branch "master"
					}
				}
				steps{
					echo "I am new to Canada"
				}	
			 }

			 stage('Four'){
				parallel{
				
					stage('Unit Test'){
						steps{
							echo "Running the unot test..."
						}	
					}


					stage('Integration Test'){

						agent{
						      docker {
							reuseNode false
							image 'ubuntu'
						      }	
						}
						steps{
							echo "Running the Integration test..."
						}	
					}
				}

			 }

		      }	

}
