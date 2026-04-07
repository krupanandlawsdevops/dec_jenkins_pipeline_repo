pipeline{
    agent any
    
    stages{
        stage('STAGE1'){
            steps{
                echo "This is stage 1 running"
                sh '''
                sleep 5
                exit 1
                '''
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