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
                withAWS(region:'ap-southeast-2',credentials:'aws-static') {
		        sh 'echo "Hello World with AWS"'
                s3Upload(file:'index.html', bucket:'jenkins-pipeline-vp', path:'index.html')
                }
            }
        }
    }
}
