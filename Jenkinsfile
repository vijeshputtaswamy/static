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
                withAWS(region:'sydney',credentials:'aws-static') {
		        sh 'echo "Hello World with AWS"'
                s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkins-pipeline-vp')
                }
            }
        }
    }
}
