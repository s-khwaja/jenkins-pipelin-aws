pipeline {
     agent any
     stages {
	stage ('Lint HTML'){
	    steps { 
		sh 'tidy -q -e *.html'
		}
        stage ('Upload to AWS') {
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
}

