pipeline {
    agent any
    stages {
       stage ('Lint HTML') {
	     steps {
		sh 'tidy -q -e *.html'
		}
	    }
       stage('Upload to AWS') {
             steps {
                 withAWS(region:'us-west-1',credentials:'jenkins-pipelin-aws') {
                 sh 'echo "Uploading content with AWS creds"'
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'sami-html-static-aws')
                 }
             }
        }
    }
}
