pipeline {
    agent {
        docker { 
            image: 'node:14-alpine'
            registryUrl: 'https://registry.hub.docker.com'
            }
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'npm run unit-test'
            }
        }
        stage('Integration test') {
            steps {
                echo 'Testing integration....'
                sh 'npm run integration-test'
            }
        }
    }
}