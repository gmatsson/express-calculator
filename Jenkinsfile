pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                npm install
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                npm run unit-test
            }
        }
        stage('Integration test') {
            steps {
                echo 'Testing integration....'
                npm run integration-test
            }
        }
    }
}