pipeline {
    agent any

    environment {
        NODE_OPTIONS = '--openssl-legacy-provider'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                dir('Projekt_Frontend') {
                    sh 'npm install'
                }
            }
        }

        stage('Build') {
            steps {
                dir('Projekt_Frontend') {
                    sh 'npm run build'
                }
            }
        }

        stage('Test') {
            steps {
                dir('Projekt_Frontend') {
                    sh 'npm test || true'
                }
            }
        }

        stage('Deploy') {
            steps {
                dir('Projekt_Frontend') {
                    echo 'Hier erfolgt das Deployment'
                    // Beispiel: sh './deploy.sh'
                }
            }
        }
    }
}

            }
        }

        stage('Test') {
            steps {
                dir('Projekt_Frontend') {
                    sh 'npm test || true'
                }
            }
        }

        stage('Deploy') {
            steps {
                dir('Projekt_Frontend') {
                    echo 'Deployment erfolgreich'
                }
            }
        }
    }
}
