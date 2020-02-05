pipeline {
    agent none
    stages {
        stage("master branch task"){
           agent { label 'master'}
            when { branch 'master'}
            steps {
                 checkout scm
                 sh "docker build -t python ."
            }
        }
        stage("develop branch"){
           agent { label 'develop'}
            when { branch 'develop'}
            steps {
                 checkout scm
                 sh "docker build -t python ."
            }
        } 
    }
}
