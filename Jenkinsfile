pipeline{
    agent any
// uncomment the following lines by removing /* and */ to enable
    tools{
       nodejs 'nodejs'
    }
    
    stages{
        stage('build'){
            steps{
                echo 'this is the build job'
                sh 'npm install'
                sleep 4
            }
        }
        stage('test'){
            steps{
                echo 'this is the test job'
                sh 'npm test'
                sleep 4
            }
        }
        stage('package'){
            steps{
                echo 'this is the package job'
                sh 'npm run package'
                sleep 4
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
