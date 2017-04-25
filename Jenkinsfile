pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sshagent (credentials: ['eberf2']) {
          sh 'ssh -o StrictHostKeyChecking=no -l eberf 192.168.20.128 ifconfig'
          sh 'scp /home/eberf/Documents/myfile.txt eberf@192.168.20.128:/home/eberf'
        }
        script {
            load "/home/eberf/params.groovy"
        }
      }
    }
    stage('Param') {
      steps {
        echo "flo: ${env.FLO}"
      }
    }
    stage('Conditional') {
        when { branch 'master'}
        steps {
            echo "on Master"
        }
    }
  }
}