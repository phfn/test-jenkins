

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'ls'
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'builded.txt', fingerprint: true
        }
    }
}

