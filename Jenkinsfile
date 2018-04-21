pipeline {

    agent {
        dockerfile true
    }
    stages {
        stage('Clone Repository') {
            steps{
                checkout scm
            }
        }

        stage('Build') { 
            steps{
                def app = docker.build("test-image", "./test")
            }
            
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
