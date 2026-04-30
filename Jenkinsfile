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
                retry(3){
                sh 'mvn test'
                }
            }

        }
    }
}