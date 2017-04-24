pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sshagent (credentials: ['eberf']) {
          sh 'ssh 192.168.20.130 echo "Hello World"'
        }
      }
    }
  }
}