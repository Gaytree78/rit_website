pipeline {
    agent any

    // Optional: remove or configure triggers
    // triggers {
    //     cron('H 2 * * *') // Uncomment to run daily at 2 AM
    // }

    stages {
        stage('Checkout') {
            steps {
                // Explicitly checkout Git repo
                git branch: 'main', url: 'https://github.com/Gaytree78/rit_website.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                // Add your build commands here, e.g., npm install, mvn package, etc.
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your test commands here
            }
        }

        stage('Archive') {
            steps {
                echo 'Archiving artifacts...'
                // Example: archive artifacts if needed
                // archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
