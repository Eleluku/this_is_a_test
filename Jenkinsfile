pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sshagent (credentials: ['eberf']) {
          sh 'ssh echo "Hello World"'
        }
      }
    }
  }
}