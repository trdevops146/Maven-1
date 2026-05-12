pipeline {
    agent any
    tools{
        maven 'mymaven'
    }
    stages{
        stage('Clonerepo'){
            steps{
                git url: 'https://github.com/trdevops146/Maven-1.git'
            }
        }
        stage('Build and compile the code'){
            steps{
                sh '''
                mvn clean install
                '''
            }
        }
        stage('Code Review'){
            steps{
                sh '''
                mvn pmd:pmd
                '''
            }
            post{
                success{
                    recordIssues sourceCodeRetention: 'LAST_BUILD', tools: [acuCobol(pattern: '**/pmd.xml')]
                }
            }
        }
    }
}