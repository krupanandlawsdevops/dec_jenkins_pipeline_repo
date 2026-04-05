pipeline{
    agent any

    environment{
        DOCKER_USER = 'krupanand'
        AWS_ACCESS_KEY = '1234567890'
    }
    
    stages{
        
        stage('STAGE1'){
            
            environment{
                STAGE = 'stage1'
            }

            steps{
                echo "DOCKER_USER : ${env.DOCKER_USER}"
                echo "AWS_ACCESS_KEY : ${env.AWS_ACCESS_KEY}"
                echo "STAGE: ${env.STAGE}"

                sh'''
                    env
                '''
            }
        }

        stage('STAGE2'){
            steps  {
                echo "DOCKER_USER : ${env.DOCKER_USER}"
                echo "AWS_ACCESS_KEY : ${env.AWS_ACCESS_KEY}"
                echo "STAGE: ${env.STAGE}"

                sh'''
                    env
                '''
            }
        }
    }
}