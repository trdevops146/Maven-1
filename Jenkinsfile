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
                script{
                    input 'Continue to test'
                }
            }
        }
        stage('Test the code'){
            steps{
                echo 'Testing the code'
                sh 'mvn test'
            }
        }
        stage('Package the code'){
            steps{
                echo 'Packing the code'
                sh 'mvn package'
            }
        }
    }
}