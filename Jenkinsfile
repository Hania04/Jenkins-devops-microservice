//Scripted Pipeline

//node {
//		echo "Build"
//		echo "Test"
//		echo "Integration Test"
//	}

//Declarative pipeline

pipeline {
	agent any
	stages{
		stage('Build'){
			steps{
			echo "Build"
			
			}
		}
		stage('Test'){
			steps{
			echo "Test"
			}
		}
		
		stage('Deploy'){
			steps{
			echo "Deploy"
			
			}
		}
		
		
	} 
	post{
			always{
			   echo "I am Good"
				}
			success{ echo 'I Run when Successfull'}
			failure { echo ' Run When Failure'} 
			
		}
	
}