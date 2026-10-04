pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Fetch the source code from the directory path specified by the environment variable"
                echo "Compile the code and generate any necessary artefacts"
            }
        }
        stage('Test') {
            steps {
                echo "Unit Tests"
                echo "Integration Tests"
            }
        }
        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy the application to a testing environment specified by the environment variable"
                echo "Testing environment ${TESTING_ENVIRONMENT}"
            }
        }
        stage('Approval') {
            steps {
                echo "waiting approval..."
                sleep 10
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploying code path '${DIRECTORY_PATH}'..."
                echo "Deployed to production environment '${PRODUCTION_ENVIRONMENT}'."
            }
        }
    }
}