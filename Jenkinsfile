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
        timestamps()
      }
    }
  }
}