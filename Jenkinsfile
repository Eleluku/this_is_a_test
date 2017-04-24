pipeline {
  agent any
  
  parameters {
    choice(choices: 'Eins\nZwei\nDrei', description: 'test', name: 'userFlag')
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
      steps {
        echo "flag: ${params.userFlag}"
      }
    }
  }
}