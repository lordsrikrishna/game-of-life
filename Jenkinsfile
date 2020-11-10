pipeline {
    agent { label 'UBUNTU' }
    triggers { pollSCM('* * * * *') }
    stages {
        stage('clone and compile')
        {
        steps {
            git branch: 'declarative'
            url: 'https://github.com/lordsrikrishna/game-of-life.git'
            sh 'mvn compile'
              }
        }
           }
}