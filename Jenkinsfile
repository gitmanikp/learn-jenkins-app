pipeline {
    agent any
    
    stages {
        stage('w/o docker') {
            steps {
                echo 'no docker!! Hence no lang version..'
            }
        }
        stage('w/ docker') {
            agent {
                    docker {
                        image 'node:18-alpine'
                    }
            }
            steps {
                sh 'echo "with docker"'
                sh 'npm --version'
            }
        }
    }
}