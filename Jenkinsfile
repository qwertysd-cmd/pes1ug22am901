pipeline {
    agent any 

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o pes1ug22am901-1 main1.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './pes1ug22am901-1'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
