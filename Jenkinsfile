pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
               git branch: 'main',
               url: 'https://github.com/Akshay-Honnavalli/PES1UG21CS065_Jenkins.git' 
            }
        }
        stage('Build') {
            steps {
                build 'PES1UG21CS065-1'
                sh 'g++ hello2.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './ash.sh'
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
