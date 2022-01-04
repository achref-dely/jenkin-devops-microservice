pipeline {
//    agent any
    agent { docker { image 'maven:3.6.3'} } // where to build
    stages {
        stage('Build') {
            steps {
                sh 'mvn --version'
                echo "Build"
            }
        }
         stage('test') {
             steps {
                echo "test"
             }
         }
         stage('Integration Test') {
             steps {
                echo "Integration Test"
             }
         }
    }

     post {
        always {
            echo "awesome i run always"
        }
        success {
            echo "i run when you success"
        }
        failure {
            echo "i run when you fail"
        }
    }
}