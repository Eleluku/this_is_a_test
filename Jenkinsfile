pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn package'
      }
    }
    stage('Publish Tests') {
      steps {
        junit(testResults: '**/target/surefire-reports/*.xml', allowEmptyResults: true)
      }
    }
    stage('AfterPublish') {
      steps {
        echo 'Done'
      }
    }
  }
}