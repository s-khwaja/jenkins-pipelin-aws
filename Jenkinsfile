pipeline {
     agent any
     stages {
        stage ('Upload to AWS') {
	    steps{
		s3Upload(file:'index.html', bucket:'sami-html-static-aws', path:'arn:aws:s3:::sami-html-static-aws/index.html')}
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell script works too"
                    ls -lah
                '''
             }
           }
       }
}

