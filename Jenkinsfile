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
        echo 'Done'
      }
    }
    stage('additional') {
      steps {
        echo 'Und noch was'
      }
    }
  }
}