pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
               git branch: 'main',
               url: 'https://github.com/Harshith48/PES1UG21CS226_Jenkins.git'  // Replace with your Git repository URL
            }
        }
        stage('Build') {
            steps {
                build 'PES1UG21CS226-1'
                sh 'g++ hello1.cp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
