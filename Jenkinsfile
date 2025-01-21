pipeline {
    agent {
        docker {
            image 'node:16' // Use a Node.js Docker image with npm pre-installed
        }
    }
    stages {
        stage("Checkout") {
            steps {
                // Checkout the code from the repository
                checkout scm
            }
        }
        stage("Test") {
            steps {
                sh 'npm install' // Install project dependencies
                sh 'npm test'    // Run tests
            }
        }
    }
}
