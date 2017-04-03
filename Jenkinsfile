pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        parallel(
          "Build": {
            echo 'Building...'
            
          },
          "And do other Stuff": {
            echo 'Paralell Building'
            
          },
          "mvnbuild": {
            sh 'sh mvn package'
            
          }
        )
      }
    }
    stage('Test') {
      steps {
        echo 'Testing...'
      }
    }
    stage('Finalise') {
      steps {
        echo 'Done'
      }
    }
    stage('additional') {
      steps {
        echo 'just do it'
      }
    }
  }
}