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
                script {   
                aversion = sh(returnStdout: true, script: "cat build.gradle  | grep  'version ='")
             }
                sh "echo faisaltwo-${aversion}"
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                echo "$aversion"
        }
    }
}
}
