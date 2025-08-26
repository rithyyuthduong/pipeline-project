pipeline {
    agent any 

    environment {
        DIRECTORY_PATH = '/path/to/code'
        TESTING_ENVIRONMENT = 'SIT223'
        PRODUCTION_ENVIRONMENT = 'SIT223_Lab'
    }

    stages {
        stage('Build'){
            steps {
                echo 'Fetch the source code from the directory path specified by the environment variable.'
                echo 'DIRECTORY_PATH: ${env.DIRECTORY_PATH}'
                echo 'Compile the code and generate any necessary artefacts.'
            }
        }

        stage('Test'){
            steps {
                echo 'Unit Tests'
                echo 'Integration tests'
            }
        }

        stage('Code Quality Checkl'){
            steps {
                echo 'Check the quality of the code'
            }
        }

        stage('Deploy'){
            steps {
                echo 'Deploy the application to a testing environment specified by the environment varaible'
                echo 'Testing environment: ${env.TESTING_DIRECTORY}'
            }
        }

        stage('Approval'){
            steps {
                echo 'Waiting 10 seconds to simulate manual approval...'
                sleep time: 10, unit: 'SECONDS'
            }
        }

        stage('Deploy to Production'){
            steps {
                echo 'Deploy code to the production environment: ${env.PRODUCTION_ENVIRONMENT}'
            }
        }
    }

    post {
        success { echo 'Pipeline completed successfully.'}
        failure { echo 'Pipeline failed.'}
    }        
}