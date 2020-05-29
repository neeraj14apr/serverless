def aversion = "test"
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo $aversion
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
