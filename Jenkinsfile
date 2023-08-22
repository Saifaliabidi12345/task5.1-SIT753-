pipeline {
    agent any 

    environment {
        DIRECTORY_PATH = '/path/to/code'
        TESTING_ENVIRONMENT = 'staging'
        PRODUCTION_ENVIRONMENT = 'SyedSaifAliAbidi'
    }

    stages {
        stage('Build') {
            steps {
                echo "Fetching source code from: ${DIRECTORY_PATH}"
                echo "Compile the code and generate artifacts."
            }
        }

        stage('Test') {
            steps {
                echo "Performing unit tests."
                echo "Performing integration tests."
            }
        }

        stage('Code Quality Check') {
            steps {
                echo "Checking code quality."
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying to: ${TESTING_ENVIRONMENT}"
            }
        }

        stage('Approval') {
            steps {
                script {
                    echo 'Waiting for approval...'
                    sleep(time: 10, unit: 'SECONDS')
                }
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "Deploying to Production: ${PRODUCTION_ENVIRONMENT}"
            }
        }
    }
}
