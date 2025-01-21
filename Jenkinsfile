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
                sh 'apt install npm'
                sh 'npm test'
            }
        }
    }
}
     
