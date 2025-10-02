pipeline {
  agent any

  stages {
    stage('Build') {
      steps { echo 'Building…' }
    }
    stage('Test') {
      steps { echo 'Running tests…' }
    }
    stage('Deploy') {
      steps { echo 'Deploy complete!' }
    }
  }

  post {
    success {
      mail to: 'sameekshashrestha14@gmail.com',
           subject: "✅ Build SUCCESS: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
           body: """The build finished successfully.

Job:   ${env.JOB_NAME}
Build: ${env.BUILD_NUMBER}
URL:   ${env.BUILD_URL}console
"""
    }
    failure {
      mail to: 'sameekshashrestha14@gmail.com',
           subject: "❌ Build FAILED: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
           body: """The build failed.

Job:   ${env.JOB_NAME}
Build: ${env.BUILD_NUMBER}
URL:   ${env.BUILD_URL}console
"""
    }
  }
}
