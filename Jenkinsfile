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
    }
}