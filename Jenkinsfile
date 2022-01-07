

pipeline {
    agent any
    stages {
        stage('ls') {
            steps {
                sh 'ls'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "build">builded.txt'
            }
        }
        stage('Test') {
            steps {
                cat builded.txt
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'builded.txt', fingerprint: true
        }
    }
}

