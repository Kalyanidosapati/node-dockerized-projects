pipeline {
    agent any
    stages {
        stage("Checkout") {
            steps {
                // Checkout the code from the repository
                checkout scm
            }
        }

        stage("Test") {
            steps {
                // Install npm if not already installed and run tests
                sh '''
                apt-get update -y
                apt-get install -y npm || true
                npm test
                '''
            }
        }

        stage("Build") {
            steps {
                // Run the build command
                sh 'npm run build'
            }
        }

        stage("Build Docker Image") {
            steps {
                // Build the Docker image
                sh 'docker build -t my-node-app:1.0 .'
            }
        }
    }
}
