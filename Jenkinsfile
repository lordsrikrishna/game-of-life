node
{
 stage('scm')
	{
		git 'https://github.com/lordsrikrishna/game-of-life.git'
	}
	stage('package')
	{
		sh 'mvn package'
	}
	stage('Sonar')
	{
		withSonarQubeEnv('Sonar-6.7.4')
		{
		sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar'
		}
	}
}
