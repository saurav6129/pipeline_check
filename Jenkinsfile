pipeline {
	
	agent any
	
	stages {
		
		stage("One") {
			
			
			steps {
				echo 'Hi this is Saurav...'
			
			}
		}
		stage("Two") {

			
			steps {
				input('Do you want to proceed further ?')
			}
		}
		
	
		stage("Three") {
		
			when {
				not {
					branch 'master'
				
				}
			}
			
			steps {
				echo 'Congrats You are at stage 3...'
			}
		}
		
		
		stage("Four") {
		
			parallel {
				stage('Unit Test'){
					steps {
						echo "Running the unit test in parallel ..."
					}
				}
			
			
				stage('Integration Test') {
					
					steps {
						echo 'Running the integration test in parallel...'
					
					}
					
				}
			}
		
		}
		
		

	}

}