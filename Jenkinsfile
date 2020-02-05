pipeline {
    agent none
    stages {
        stage("master branch task"){
            when {
                branch 'master'
            }
            agent { label 'master'}
            steps {
                 echo "on master branch"
                 sh "sh sample.sh"
            }
        }
        stage("develop branch"){
            when {
                branch 'develop'
            }
            agent { label 'develop'}
            steps {
                echo "on $BRANCH_NAME branch"
            }
        }
    }
}
