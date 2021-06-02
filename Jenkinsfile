//Scripted Pipeline

//node {
//		echo "Build"
//		echo "Test"
//		echo "Integration Test"
//	}

//Declarative pipeline

pipeline {

		agent any
		environment{
		dockerHome = tool 'MyDocker'
		mavenHome =  tool 'Maven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
		}
		//agent { docker { image 'maven:3.6.3'} }
	stages{
		stage('Build'){
			steps{
			sh 'mvn --version'
			sh 'docker version'
			echo "PATH - $PATH"
			echo "BUILD_NUMBER - $env.BUILD_NUMBER"			
			echo "BUILD_ID - $env.BUILD_ID"
			echo "JOB_NAME - $env.JOB_NAME"
			echo "BUILD_URL -$env.BUILD_URL"
			echo "BUILD_TAG - $env.BUILD_TAG"
			
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