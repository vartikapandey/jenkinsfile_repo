pipeline {
    agent any
    stages {
        stage('init stage'){
            steps{
                bat '''
                set
                echo "init stage ran successfully"
                '''
            }
        }
        stage('parallel_stage') {
            parallel {
                stage('first parallel stage'){
                    bat '''
                        echo %JENKINS_HOME%
                    '''
                    build job: 'basicCI'
                }
            }
        }
    }
}