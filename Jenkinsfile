pipeline {
    agent none

    stages {
        stage("master branch tasks"){
           agent {
                label "master"
            }
            when {
                beforeAgent true
                branch 'master'
            }
            steps {
                echo "$BRANCH_NAME"
            }

            steps {
                 echo "on master branch"
                 sh "sh sample.sh"
            }
        }
    
    stages {
        stage("master branch tasks"){
           agent {
                label "develop"
            }
            when {
                beforeAgent true
                branch 'develop'
            }
            steps {
                echo "on $BRANCH_NAME branch"
            }

            steps {
                 echo "on $BRANCH_NAME branch"
            }
        }
    }
}
