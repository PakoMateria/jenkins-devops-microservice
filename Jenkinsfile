//SCRIPTED

//DECLARATIVE
pipeline {
	//agent any
	agent { docker { image 'maven:3.6.3'} }
	stages {
		
            	stage('Permission') {
			steps {
				sh "sudo chown root:jenkins /run/docker.sock"
				sh "sudo chown root:jenkins /var/run/docker.sock"
				sh "sudo chown root:jenkins /usr/local/bin/docker"
			}
		}
		stage('Build') {
			steps {
				sh 'mvn --version'
				echo "Build"
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}
		}
		stage('Integration Test') {
			steps {
				echo "Integration Test"
			}
		}	
	} 
	
	post {
		always {
			echo "I'm awesome, I run always"
		}
		success {
			echo "I run when you are successful"
		}
		failure {
			echo "I run when you fail"
		}
	}
}
