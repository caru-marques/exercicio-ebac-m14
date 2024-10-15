pipeline {
    agent any

    stages {
        stage('Setup') {
            steps {
                git branch: 'main', url: 'https://github.com/caru-marques/exercicio-ebac-m14'
            }
        }
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Start Server') {
            steps {
                sh 'npm run start'
            }
        }
        stage('Test') {
            steps {
                sh 'NO_COLOR=1 npm run cy:run'
            }
        }
    }
}
