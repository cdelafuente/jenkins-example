pipeline {
  agent { docker 'php' }
  stages {
    stage('Build') {
      steps {
        sh 'php --version'
      }
    }
    stage('Test') {
      steps {
        sh 'echo "Fail"'
        sh 'exit 1'
      }
    }
  }
  post {
    always {
      sh 'This will always run'
    }
    success {
      sh 'This will run only if successful'
    }
    failure {
      sh 'This will run only if failed'
    }
    unstable {
      sh 'This will run only if the run was marked as unstable'
    }
    changed {
      sh 'This will run only if the run was marked as unstable'
      sh 'For example, the Pipeline was previously failing but is now successful'
    }
  }
}
