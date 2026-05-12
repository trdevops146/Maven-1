pipeline{
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
        stage('Build and compile code'){
            steps{
                sh '''
                mvn build
                '''
            }
        }

    }
}
