pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       maven 'maven' 
    }
   

    stages{
        stage('build'){
            steps{
                echo 'this is the build job'
                sh 'compile'
                
            }
        }
        stage('test'){
            steps{
                echo 'this is the testjob'
                sh 'clean test'
                
            }
        }
        stage('package'){
            steps{
                echo 'this is the package job'
                sh 'package -DskipTests'
             
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
