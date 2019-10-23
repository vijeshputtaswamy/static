pipeline {
  agent any
  stages {
    stage('Say Hello - Build init') {
      steps {
        sh 'echo "Hello World - Vijesh Puttaswamy"'
        sh '''
                  echo "Multi-line works too!"
                  ls -lrtha
                '''
      }
    }
  }
}     
