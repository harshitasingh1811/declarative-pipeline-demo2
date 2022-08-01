pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        echo "this is build ${BUILD_NUMBER} and ${DEMO}"
        sh'''
          echo"running a shell script"
          chmod +x test.sh
          test.sh
          
          '''
      }
    }

  }
  environment {
    DEMO = '1'
  }
}
