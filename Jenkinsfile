pipeline {
    agent any

    stages {
        stage('w/o docker') {
            steps {
                sh '''
                    echo "without docker"
                    ls -la
                    touch containter-no.txt
                '''
            }
        }
        
        stage('w/ docker') {
            agent {
                docker {
                    image 'node:18-alpine'
                }    
            }    
            steps {
                sh '''
                    echo "without docker"
                    ls -la
                    touch containter.txt
                '''
            }
        }
    }
}
