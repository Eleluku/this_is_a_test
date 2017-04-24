pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sshagent (credentials: ['eberf2']) {
          sh 'ssh -o StrictHostKeyChecking=no -l eberf 192.168.20.128 ifconfig'
        }
        sh 'ifconfig'
      }
    }
  }
}