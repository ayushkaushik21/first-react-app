pipeline {
    agent any
    stages {
        stage('Package Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                sh 'npm run test'
            }
        }
        stage('Deliver') { 
            steps {
                sh 'nohup serve -s build &' 
            }
        }
    }
}