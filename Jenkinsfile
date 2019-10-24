pipeline {
  agent any
  stages {
    stage('Lint HTML') {
            steps {
                sh 'tidy -q -e *.html'
            }
        }
    stage('Upload to AWS') {
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
