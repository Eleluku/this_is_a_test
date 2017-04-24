pipeline {
  agent any
  
  parameters {
    booleanParam(defaultValue: true, description: 'test', name: 'userFlag')
  }
  stages {
    stage('Build') {
      steps {
        sshagent (credentials: ['eberf2']) {
          sh 'ssh -o StrictHostKeyChecking=no -l eberf 192.168.20.128 ifconfig'
          sh 'scp /home/eberf/myfile.txt eberf@192.168.20.128:/home/eberf'
        }
      }
    }
    stage('Param') {
        echo "flag: ${params.userFlag}"
    }
  }
}