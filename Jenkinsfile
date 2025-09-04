pipeline {
  agent any
  triggers {
    // pick ONE: daily at 10:00 or on GitHub webhook
    // cron('H 10 * * *')
    // githubPush()  // works when GitHub webhook is configured
  }
  stages {
    stage('Checkout') {
      steps { checkout scm }
    }
    stage('Build') {
      steps {
        bat 'node -v && npm -v'
        bat 'npm ci'
        bat 'npm run build'
      }
    }
    stage('Archive') {
      steps {
        archiveArtifacts artifacts: 'dist/**, build/**, **/*.html, **/*.css, **/*.js', fingerprint: true
      }
    }
  }
}
