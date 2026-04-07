pipeline{
    agent any
    
    stages{
        stage('STAGE1_a'){
            steps{
                catchError(buildResult :'Success', stageResult : 'FAILURE'){
                    echo "This is stage 1 running"
                    sh '''
                        sleep 5
                        exit 1
                    '''
                    }
            }
        }

        stage('STAGE1_b'){
            steps{
                script{
                    try{
                        sh'''
                        sleep 5
                        exit 1
                        '''
                    }
                    catch(err){
                        echo "Error caught : ${err}"
                        currentBuild.result = 'SUCCESS'
                    }
                }
                    
            }
        }

        stage('PARALLEL TESTING'){
            parallel {
                stage('WINDOWS TESTING') {
                    steps{
                        echo "This is windows testing running"
                        sh 'sleep 10'
                    }  
                }

                stage('MAC TESTING') {
                    steps{
                        echo "This is mac testing running"
                        sh 'sleep 10'
                    }  
                }
            }
        }

        stage('FINAL'){
            steps{
                echo 'This is final running'
                sh 'sleep 5'
            }
        }
    }
}