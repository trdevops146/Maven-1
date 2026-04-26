pipeline {
    agent any
    environment{
        APP_NAME = "mydemoapp"
        APP_URL = "console.amazon.com"
    }
    stages{
        stage('Using the variables defined'){
            steps{
                echo "app name is ${APP_NAME}"
            }
        }
    }
}