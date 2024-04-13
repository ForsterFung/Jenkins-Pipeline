pipeline{
    agent any
    environment {
        DIRECTORY_PATH = "C:/ProgramData/Jenkins/.jenkins/workspace/SIT223_SIT753-5.1P"
        TESTING_ENVIRONMENT = "dev"
        PRODUCTION_ENVIRONMENT = "prd"
    }
    stages{
        stage('build'){
            steps{
                echo "DIRECTORY_PATH: $DIRECTORY_PATH"
                echo "compile the code and generate any necessary artifacts"
            }
        }

        stage('test'){
            steps{
                echo "unit tests"
                echo "integration tests"
            }
        }

        stage('code_quality_check'){
            steps{
                echo "check the quality of the code"
            }
        }

        stage('deploy'){
            steps{
                echo "deploy the application to a testing environment specified by the environment variable"
            }
        }

        stage('approval'){
            steps{
                sleep 10
            }
        }

        stage('deploy_to_production'){
            steps{
                echo "PRODUCTION_ENVIRONMENT: $PRODUCTION_ENVIRONMENT"
            }
        }
    }
}