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
            sh 'mvn package'
            
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
        parallel(
          "additional": {
            echo 'just do it'
            
          },
          "junit": {
            junit(testResults: 'GitTest/target/surefire-reports/*', allowEmptyResults: true)
            
          }
        )
      }
    }
  }
}