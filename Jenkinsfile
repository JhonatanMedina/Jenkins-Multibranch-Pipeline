#!Jenkins-Multibranch-Pipeline2


pipeline {
	agent any
	environment {
       	 EXECUTE = "true"
   	}
		stages {
			stage('First') {
				steps {
					echo "${execute}
					sh '''
						echo "Step One"
					'''
				}
			}


			stage('Second') {
				when {
					environment name: "execute" , value: "true"	
				}
				
				steps {
					sh '''
						echo "Updating Second Stage"
					'''
				}
			} 

			stage('Third') {
				steps {
					sh '''
						echo "Step Three"
					'''
				}
			}
		}
}



