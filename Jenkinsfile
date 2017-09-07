pipeline {
  agent any
  stages {
    stage('Checkout Sources') {
      steps {
        echo 'hello world'
      }
    }
    stage('Build') {
      steps {
        parallel(
          "Build": {
            sh 'echo "This is a build step 1"'
            
          },
          "Build2": {
            sh 'echo "Build step 2"'
            
          },
          "Build3": {
            echo 'build step3'
            
          }
        )
      }
    }
    stage('Test') {
      steps {
        parallel(
          "Test": {
            echo 'test1'
            
          },
          "Test1": {
            sh 'echo "executing Test1"'
            
          },
          "Test2": {
            sh 'echo "Executing Test2"'
            
          }
        )
      }
    }
    stage('Final') {
      steps {
        echo 'Done'
      }
    }
  }
}