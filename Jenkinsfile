pipeline {
    agent { label 'UBUNTU' }
	triggers {
	   upstream(upstreamProjects: 'dummy', threshold: hudson.model.Result.SUCCESS)
	}
    stages {
        stage('Source'){
            steps {
                git 'https://github.com/lordsrikrishna/game-of-life.git' 
            }
        }
        stage('Package'){
            steps {
                sh 'mvn package'
            }
        }
    }
}
