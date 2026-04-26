pipeline{
    agent any
    stages{
        stage('Build the code'){
            when{ 
                expression{
                    params.environment == 'dev'
                }
            }
            steps{
                sh 'mvn build'
            }

        }
    }
}