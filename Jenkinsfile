pipeline {
    agent any
    tools{
        maven "mymaven"
    }
    stages{
        stage('Clone github repo'){
            steps{
                echo 'Cloning the github repo'
                git 'https://github.com/trdevops146/Maven-1.git'

            }
        }
        stage('Compile the code'){
            steps{
                echo 'Cloning the github repo'
                sh 'mvn compile'
            }
        }
    }
}