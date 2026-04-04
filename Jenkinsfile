pipeline{
    agent {label 'slave1'}

    stages{a
        stage('STAGE1'){
            steps{
                echo "This is stage1"
                sh '''
                    sleep 10
                    echo "This is a linux command"
                '''
            }
        }
        stage('STAGE2'){
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