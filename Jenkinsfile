pipeline {
    agent any

    parameters {
        booleanParam(name: 'executeTests', defaultValue: true)
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }

        stage('Test') {
            when {
                expression { params.executeTests == true }
            }
            steps {
                echo 'Testing..'
            }
        }
    }
}
