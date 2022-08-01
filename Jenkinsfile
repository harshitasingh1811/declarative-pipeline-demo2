pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        bat '"this is build ${BUILD_NUMBER} and ${DEMO}"'
      }
    }

  }
  environment {
    DEMO = '1'
  }
}