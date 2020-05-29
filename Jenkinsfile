def aversion = "test"
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                aversion = sh(returnStdout: true, script: "cat build.gradle  | grep  'version ='")
                sh "echo faisaltwo-${aversion}"
             }
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                echo $aversion
            }
        }
    }
}
