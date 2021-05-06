pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       maven 'maven' 
    }
    

    stages{
        stage('build'){
            steps{

                sh 'mvn compile'
            }
        }
        stage('test'){
            steps{

                sh 'mvn clean test'
            }
        }
        stage('package'){
            steps{

                sh 'mvn package -DskipTests'
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
