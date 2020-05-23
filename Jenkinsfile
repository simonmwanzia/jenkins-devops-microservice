//pipeline
// node {
	
// 		echo "Build"
	
// 		echo "Test"
	
// 		echo "Test"
	
// }

//scripted

// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 	stage('Integration Test') {
// 		echo "Test"
// 	}
// }

pipeline {
	//agent any
	agent {docker {image "maven:3.6.3"}}
	stages{
		stage("Build"){
			steps{
				sh "mvn --version"
				echo "Build"				
			}
		}
		stage("Test"){
			steps{				
				echo "Test"			
			}
		}
		stage("Integration Test"){
			steps{				
				echo "Integration Test"
			}
		}
	}

	post{
		always{
			echo "i am awesome.i run always"
		}
		success{
			echo "i run when you are successful"
		}
		failure{
			echo "i run when you fail"
		}
	}

	
		
	
}