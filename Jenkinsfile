pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sshagent (credentials: ['eberf2']) {
          sh 'ssh -o StrictHostKeyChecking=no -l eberf 192.168.20.128 echo "Hello World"'
          sh 'uname -a'
          sh 'exit'
          sh 'uname -a'
        }
      }
    }
  }
}