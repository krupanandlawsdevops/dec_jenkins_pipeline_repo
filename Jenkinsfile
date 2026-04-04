pipeline{

    agent none

    parameters{
        string(name: 'NAME', defaultValue: '', description: 'please tell me ur name')
        booleanParam(name: 'SKIP_TEST', description: 'want to skip the test runs to direct deploy')
        choice(name: 'BRANCH', choices: ['master','staging','prod'], description: '')
    }
    
    stages{
        
        stage('STAGE1'){
            
            agent {label 'slave1'}

            steps{
                echo "NAME : ${params.NAME}"
                echo "SKIP_TEST : ${params.SKIP_TEST}"
                echo "BRANCH TO DEPLOY : ${params.BRANCH}"
            }
        }
    }
}

// pipeline {
//     agent none

//     stages {
//         stage('Run on both nodes') {
//             parallel {

//                 stage('Run on slave1') {
//                     agent { label 'slave1' }
//                     steps {
//                         echo "Running on slave1"
//                         sh '''
//                             sleep 10
//                             echo "This is a linux command"
//                             hostname
//                         '''
//                     }
//                 }

//                 stage('Run on slave2') {
//                     agent { label 'slave2' }
//                     steps {
//                         echo "Running on slave2"
//                         sh '''
//                             sleep 10
//                             echo "Building Java Code"
//                             hostname
//                         '''
//                     }
//                 }

//             }
//         }
//     }
// }