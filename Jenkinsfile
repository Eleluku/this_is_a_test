pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sshagent (credentials: ['eberf']) {
          sh 'ssh -o StrictHostKeyChecking=no -l eberf 192.168.20.128 uname -a echo "Hello World"'
        }
      }
    }
  }
}