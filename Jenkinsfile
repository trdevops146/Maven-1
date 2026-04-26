pipeline{
    agent any
    stages{
        stage('Build the code'){
            when{ 
                expression{
                    params.env == 'dev'
                }
            }
            steps{
                sh 'mvn build'
            }

        }
    }
}