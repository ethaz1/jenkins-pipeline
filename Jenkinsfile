pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Compile the code from the GitHub repo. This produces the usable/executable program. A tool like Maven can be used, which automatically fetches"
                echo "packages and executes the given build steps."
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo "Run unit and integration tests to check for bugs, vulnerabilities and regressions. JUnit can be used for this purpose, and Maven can actually run JUnit"
                echo "after it successfully builds by running 'mvn test'."
            }
        }
        stage('Code Analysis') {
            steps {
                echo "Analyse the code for bugs, code smells, vulernabilities, and coding-standard issues. Things like dead code, hard-coded credentials, SQL injection, etc." 
                echo "which runtime testing could not pick up. SonarQube is often integrated into CI/CD pipelines for this purpose."
            }
        }
        stage('Security Scan') {
            steps {
                echo "Analyse third-party dependencies used by the application and ensure they are up to date. Old dependencies may have known security exploits which"
                echo "make the program less secure. OWASP Dependency-Check is an SCA tool which can detect on bad dependencies and be integrated into a Jenkins pipeline."
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo "Deploy the build program to a temporary staging environment which resembles the real production environment. This may need databases and third-party services"
                echo "available to it to simulate such an evironment. AWS EC2 is a service which allows setting up multiple VMs to do this automatically. We might also use this in our production environment."
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo "Run integration tests in the staging environment. Unlike stage 2, which was run on individual components, this step tests the cohesive system, and often finds"
                echo "regressions where components fail to communicate with each other. Selenium is an example of a validation tool for web applications, which is used with a testing framework like JUnit."
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploy the application to a production server so it can be accessed by end-users. AWS EC2 is often used to host web applications."
            }
        }
    }
}