pipeline{
	agent {label 'agent2'}
	stages{
		stage('gitcheckout'){
		  steps{
			git branch: 'release', url: 'https://github.com/aithalias/java_repo1.git'
		    }
		}
		stage('build'){
			steps{
			 sh "mvn clean install"
			}
		}
		stage('archive'){
			steps{
			 archiveArtifacts artifacts: 'target/*.war'
			}
		}
	}
}
