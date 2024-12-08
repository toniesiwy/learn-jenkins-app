pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNdoe true
                }    
            }    
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    npm ci
                    nmp run build
                    ls -la
                '''
            }
        }
    }
}
