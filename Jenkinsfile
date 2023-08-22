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
                echo "Retrieving source code from directory: ${CODE_DIR_PATH}"
                echo "Building the source code and creating components."
            }
        }

        stage('Test') {
            steps {
                echo "Executing unit validations."
                echo "Executing system/integration validations."
            }
        }

        stage('Code Quality Check') {
            steps {
                echo "Checking source code integrity."
            }
        }

        stage('Deploy') {
            steps {
                echo "Initiating deployment to: ${TEST_ENV_NAME}"
            }
        }

        stage('Approval') {
            steps {
                script {
                    echo 'Paused for approval...'
                    sleep(time: 10, unit: 'SECONDS')
                }
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "Pushing to Live Environment: ${LIVE_ENV_NAME}"
            }
        }
    }
}
