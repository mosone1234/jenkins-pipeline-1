pipeline {
  agent { label 'master' }
  environment {
    appName = "variable"
  }
  stages {
    stage("step 1") {
      steps {
        script {
          sh "echo 'Hello world'"
        }
      }
    }
  }
  post {
    always {
      deleteDir()
      sh "echo 'fase always'"
    }
    success {
      sh "echo 'fase success'"
    }
    failure {
      sh "echo 'fase failure'"
    }
  }
}
