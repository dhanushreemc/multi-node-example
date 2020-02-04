pipeline {
    agent none
    stages {
        stage("master branch task"){
           agent {
                label "master"
            }
            when {
                beforeAgent true
                branch 'master'
            }
            steps {
                 echo "on master branch"
                 sh "sh sample.sh"
            }
        }
        stage("develop branch"){
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
        }
    }
}
