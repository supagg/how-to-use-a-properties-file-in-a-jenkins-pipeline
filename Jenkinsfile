pipeline {
    agent any

    stages {

        stage('Setup Variables') {
            steps {
                script {
                    //Get variables from project deployment.properties
                    configProperties = readProperties file: './config.properties'

                    //Get variables
                    PROJECT_AUTHOR = configProperties['DEPLOY_TO_AZURE']
                    PROJECT_BLOG = configProperties['PROJECT_BLOG']
                }

                echo "Project Author: ${PROJECT_AUTHOR}"
                echo "Project Blog: ${PROJECT_BLOG}"
            }
        }
    }
}