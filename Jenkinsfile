pipeline {
    agent {
        label 'agent1'
    }
    environment { 
        COURSE = 'jenkins'
    }
    //Build, Test, Deploy
    stages {
        stage ('Build') {
            steps {
                script{
                    sh """
                        echo "Hello Build"
                        env
                    """
                }
            }
        }
        stage ('Test') {
            steps {
                script{
                    echo 'Testing..'
                }
            }
        }
        stage ('Deploy') {
            steps {
                script{
                    echo 'Deploying..'
                }
            }
        }
    }
     post { 
        always { 
            echo 'I will always say Hello again!'
            deleteDir()
        }
        success { 
            echo 'Hello Success'
        }
        failure { 
            echo 'Hello Failure'
        }
    }
}
