pipeline{
    // agent { label 'slave1 && slave2'}
    // agent { label 'slave1 || slave2'}
    agent {'!master'}
    
    stages{
        
        stage('STAGE1'){

            steps{
                echo "This is stage1"
                sh '''
                    sleep 10
                    echo "This is a linux command"
                '''
            }
        }
        stage('Build'){

            steps{
                echo "Building Java Code"
                sh '''
                    #!/bin/bash
                    sleep 10
                '''
            }
        }
    }
}