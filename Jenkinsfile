pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo 'Building...'
      }
    }
    stage('Test') {
      steps {
        echo 'Running tests...'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy complete!'
      }
    }
  }

  post {
    success {
      mail to: 'sameekshashrestha14@gmail.com',
           subject: '✅ Build Success',
           body: 'Your Jenkins build completed successfully.'
    }
    failure {
      mail to: 'sameekshashrestha14@gmail.com',
           subject: '❌ Build Failed',
           body: 'The Jenkins build failed.'
    }
  }
}
