pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    eccho 'Compiling the C++ file...'
                    sh "g++ -o PES1UG21CS372-1 PES1UG21CS372.cpp"
                }
            }
        }
    
        stage('Test') {
            steps {
                script {
                    echo 'Running the C++ program...'
                    sh "./PES1UG21CS372-1"
                }
            }
        }

        stage('Deploy') {
            steps {
                 echo 'Deployment stage'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
