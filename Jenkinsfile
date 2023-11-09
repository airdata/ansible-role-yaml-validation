pipeline {
   agent any
   stages {
        stage('molecule') {
            steps {
                sh '''
                   docker run --rm --tty -v /var/run/docker.sock:/var/run/docker.sock -v "$(pwd)":/molecule airdata/ansible-molecule:working /bin/sh -c "molecule converge"
                '''
            }
        }     
    }
}
