pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sshagent (credentials: ['eberf']) {
          sh 'ssh eberf@192.168.20.128 echo "Hello World"'
        }
      }
    }
  }
}