pipeline{
    agent{
        node{
            label 'docker-agent-alpine'
        }
    }
    triggers{
        pollSCM('H/5 * * * *')
    }
    stages{
        stage('build'){
            steps{
                echo "Building...."
                sh '''
                echo "Doing build stuff.."
                cat build.txt
                '''
            }
        }
        stage('Test'){
            steps{
                echo "Testing...."
                sh '''
                echo "Doing test stuff.."
                cat test.txt
                '''
            }
        }
        stage('Deliver'){
            steps{
                echo "Delivring...."
                sh '''
                echo "Doing deliver stuff.."
                cat deploy.txt
                '''
            }
        }
    }
}