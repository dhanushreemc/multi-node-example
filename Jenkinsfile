pipeline {
    agent none
    stages {
        stage("master branch task"){
            steps {
                 when { branch 'master'}
                 agent { label 'master'}
                 checkout scm
                 sh "docker build -t python ."
            }
        }
        stage("develop branch"){
            steps {
                 agent { label 'develop'}
                 when { branch 'develop'}
                 checkout scm
                 sh "docker build -t python ."
            }
        } 
    }
}
