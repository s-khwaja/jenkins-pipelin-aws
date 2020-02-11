pipeline {
    agent any
    stages {
       stage ('Build') {
	     steps {
		sh 'echo "Hello world"'
		sh '''
			echo "Mulitline shell steps works too"
		'''
		}
	    }
       stage('Upload to AWS') {
             steps {
                 withAWS(region:'us-west-1',credentials:'Jenkins') {
                 sh 'echo "Uploading content with AWS creds"'
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'sami-html-static-aws')
                 }
             }
        }
    }
}
