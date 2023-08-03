pipeline {
agent any
stages {
	stage('Build') {
	parallel {
		stage('Build') {
		steps {
			sh 'echo "building the repo"'
		}
		}
	}
	}

	stage('Test') {
	steps {
		
		echo "testing the application"
	}
	}

	stage('Deploy')
	{
	steps {
		sh 'python sample.py'
		echo "deploying the application"
		
	}
	}
	stage('Final-Test') {
	steps {
		echo "testing the application"
	}
	}
}

post {
		always {
			echo 'The pipeline completed'
			
		}
		success {				
			echo "Flask Application Up and running!!"
		}
		failure {
			echo 'Build stage failed'
			error('Stopping early…')
		}
	}
}
