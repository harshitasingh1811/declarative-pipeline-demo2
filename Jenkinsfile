pipeline {
  agent any
   environment {
    
     RELEASE='20.04'
  }
  stages {
    stage('Build') {
      environment{
        LOG_LEVEL='INFO'
        }
      steps {
        echo "Building Release ${RELEASE} with log level ${LOG_LEVEL}"  
      }
    }
    stage('Test'){
      steps{
        echo "Testing Release ${RELEASE}"
        writeFile file: 'test-results.txt' , text: 'passed'
      }
 
    }

  }
  post{
    sucsess{
      archieveArtifacts 'test-results.txt'
    }
  }
  
}
