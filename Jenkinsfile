pipeline{
	agent {labe 'agent2'}
	stages{
		stage('gitcheckout'){
		  steps{
			git branch: 'dev', url: 'https://github.com/aithalias/java_repo1.git'
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
		stage('Monitoring'){
			steps{
			 echo "Being monitored by prometheus"
			}
		}
	}
}
