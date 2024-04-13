pipeline{
    agent any
    environment {
        DIRECTORY_PATH = "C:/ProgramData/Jenkins/.jenkins/workspace/SIT223_SIT753-5.1P"
        TESTING_ENVIRONMENT = "dev"
        PRODUCTION_ENVIRONMENT = "prd"
    }
    stages{
        stage('Build'){
            steps{
                echo "DIRECTORY_PATH: $DIRECTORY_PATH"
                echo "compile the code and generate any necessary artifacts"
            }
        }

        stage('Unit_and_Integration_Tests'){
            steps{
                echo "unit tests"
                echo "integration tests"
            }
        }

        stage('Code_Analysis'){
            steps{
                echo "check the quality of the code"
            }
        }

        stage('Security_Scan'){
            steps{
                echo "deploy the application to a testing environment specified by the environment variable"
            }
        }

        stage('Integration_Tests_on_Staging'){
            steps{
                sleep 10
            }
        }

        stage('Deploy_to_Production'){
            steps{
                echo "PRODUCTION_ENVIRONMENT: $PRODUCTION_ENVIRONMENT"
            }
        }
    }
}