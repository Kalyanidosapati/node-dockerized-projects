pipeline {
    agent any
    stages {
        stage("Checkout") {
            steps {
                // Checkout the code from the repository
                checkout scm
            }
        }
        stage("Test"){
            steps{
                sh 'sudo apt update && sudo apt install -y npm'
                sh 'npm install'
                sh 'npm test'
            }
        }
    }
}
     
