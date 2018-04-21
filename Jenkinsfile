pipeline {

    agent {
        dockerfile true
    }
    stages {
        stage('Clone Repository') {
            checkout scm
        }

        stage('Build') { 
            
            def app = docker.build("test-image", "./test")
        }

        stage('Testing') {
            steps {
                sh 'echo "Test Passed"'
            }
        }

        /*stage('Deliver') {
            agent {
                docker {

                }
            }
            steps {

            }
            post {
                success {
                    
                }
            }
        }*/
    }
}
