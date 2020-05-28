pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                emp = neeraj
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                echo testing id done by ${emp}
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
