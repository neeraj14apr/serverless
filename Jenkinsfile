def aversion = "test"
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage ('variable') {
      steps {
          script {    
          aversion = sh(returnStdout: true, script: "cat build.gradle  | grep  'version ='")
        }
            sh "echo faisaltwo-${aversion}"
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
