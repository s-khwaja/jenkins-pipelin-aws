pipeline {
     agent any
     stages {
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

