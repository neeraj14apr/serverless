def aversion = "test"
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps { 
                sh '''  
                aversion = sh(returnStdout: true, script: "ls -l")
                sh "echo faisaltwo-${aversion}"
                echo 'Testing..'
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
        }
    }
}
}
