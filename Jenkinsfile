pipeline{
    agent any
    
    stages{
        stage('Build'){
            steps{
                echo "Codes for building...... "
                // The build automation tool, Maven, can be used
            }
        }

        stage('Unit_and_Integration_Tests'){
            steps{
                echo "Codes to run unit tests and integration tests......"
                // The testing frameworks, JUnit or TestNG, can be applied
            }
        }

        stage('Code_Analysis'){
            steps{
                echo "Codes for analysis......"
                // The code analysis tool, SonarQube, is suitable for integration
            }
        }

        stage('Security_Scan'){
            steps{
                echo "Codes for security scanning......"
                // OWASP ZAP is a security scanning tool available in this stage
            }
            post{
                // notification emails
                success{
                    emailext to: "forsterfung@gmail.com",
                    subject: "Build Status Email",
                    body: "Build was successful!",
                    attachLog: true
                }
                failure{
                    emailext to: "forsterfung@gmail.com",
                    subject: "Build Status Email",
                    body: "Build was failure!",
                    attachLog: true
                }
             }
         }

        stage('Deploy_to_Staging'){
            steps{
                echo "Codes for deploying the application to a staging server......"
                // Example for staging server: AWS EC2 instance (DEV/UAT environment)
            }
        }

        stage('Integration_Tests_on_Staging'){
            steps{
                echo "Codes to perform integration tests on the staging environment......"
                // Conduct system integration testing on the staging server
            }
        }

        stage('Deploy_to_Production'){
            steps{
                echo "Codes for the production deployment......"
                // Deploy the application to the production server (e.g. AWS EC2 instance of Prod environment)
            }
        }
    }
}