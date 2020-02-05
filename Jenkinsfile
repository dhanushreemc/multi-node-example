pipeline {
    agent none
    stages {
        stage("master branch task"){
          when { branch 'master'} 
            agent { label 'master'}
            steps {
                 echo "running on $NODE_NAME"
                 echo "on master branch"
                 sh "sh sample.sh"
                 echo "running on $NODE_LABELS"
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
