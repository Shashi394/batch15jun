pipeline
{
	agent any
	stages
	{
		stage('Checkout')
		{
			steps
			{
				git 'https://github.com/iamdevopstrainer/DevOpsClassCodes'
			}
		}
		
			stage('Test')
		{
			steps
			{
				dir('')
				{
					sh '/var/lib/jenkins/tools/hudson.tasks.Maven_MavenInstallation/Maven361/bin/mvn test'
				}
			}
		}
		stage('Build')
		{
			steps
			{
				dir('')
				{
					sh '/var/lib/jenkins/tools/hudson.tasks.Maven_MavenInstallation/Maven361/bin/mvn package'
				}
			}
		}
		
		stage('Deployment')
		{
			steps
			{
					echo "Deployment"
					sh 'sudo cp /var/lib/jenkins/workspace/PipelineJob/target/addressbook.war /usr/share/tomcat/webapps/'
			
			}
		}
	}
		
}
