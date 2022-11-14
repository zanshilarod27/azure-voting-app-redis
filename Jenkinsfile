pipeline{
	agent any
	stages{
		stage("Verify Branch"){
			steps{
				echo "$GIT_BRANCH"
			}
		}
		stage("Docker Build"){
			steps{powershell 'docker images -a'
			      powershell 'cd azure-vote/'
			      powershell 'docker images -a'
			      powershell 'docker build -t jenkins-pipeline .'
			      powershell 'docker images -a'
			      powershell 'cd ..'
			}
		}
	} 
}
