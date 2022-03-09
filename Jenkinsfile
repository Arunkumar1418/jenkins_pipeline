// DECLARATIVE
pipeline {
	agent any 
	
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'MAVEN_HOME'
		PATH = "$mavenHome/bin:$dockerHome/bin:$PATH"
	}

	stages {
		stage('Build') {
			steps {
				sh 'mvn --version'
				sh 'docker version'
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"
			}
		}
	}
}