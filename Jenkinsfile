pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            } // end steps
        } // end stage

        stage('Test') {
            steps {
                echo 'Testing...'
            } // end steps
        } // end stage
    } // end stages

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    } // end post
} // end pipeline
