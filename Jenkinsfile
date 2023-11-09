pipeline {
   options {
       skipDefaultCheckout(true)
       ansiColor('xterm')
   }
   agent any
   
   stages {
        stage('Checkout') {
            steps {
                cleanWs()
                checkout scm
            }
        }      
        stage('molecule') {
            steps {
                sh '''
                   docker run --rm --tty -v /var/run/docker.sock:/var/run/docker.sock -v "$(pwd)":/molecule airdata/ansible-molecule:working /bin/sh -c "molecule converge"
                '''
            }
        }     
    }
}
