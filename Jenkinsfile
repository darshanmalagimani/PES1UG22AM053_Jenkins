pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ main.cpp -o PES1UG22AM053-1'
            }
        }

        stage('Test') { 
            steps {
                sh './PES1UG22AM053-1_Invalid'
            }
        }

        stage('Deploy') {
            steps { 
                echo 'Deployment Stage.'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline Failed.'
        }
    }
}
  
