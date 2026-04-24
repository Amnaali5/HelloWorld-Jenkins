pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    environment {
        NEW_VERSION = "1.3.0"
    }
    parameters {
        booleanParam(name: 'executeTests', defaultValue: true)
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building Project'
                echo "Building version ${NEW_VERSION}"

                // Windows vs Linux
                bat 'echo Installing dependencies'
                // if Linux/mac:
                // sh 'echo Installing dependencies'
            }
        }

        stage('Test') {
            when {
                expression { params.executeTests == true }
            }
            steps {
                echo 'Testing...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }

    post {
        always {
            echo 'Pipeline Finished'
        }
    }
}    
