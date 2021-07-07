pipeline {
    agent any

    stages {

        stage('Setup Variables') {
            steps {
                script {
                    //Get variables from project deployment.properties
                    configProperties = readProperties file: './config.properties'

                    //Get variables
                    PROJECT_AUTHOR = configProperties['PROJECT_AUTHOR']
                    PROJECT_BLOG = configProperties['PROJECT_BLOG']
                }

                echo "Project Author: ${PROJECT_AUTHOR}"
                echo "${configProperties.PROJECT_AUTHOR}"
                echo "Project Blog: ${PROJECT_BLOG}"
            }
        }
        stage('Use environment variable') {
            steps {
                bat "if not exist C:\\Users\\sagar\\${PROJECT_AUTHOR} md  C:\\Users\\sagar\\${PROJECT_AUTHOR}"
            }
        }
    }
}
