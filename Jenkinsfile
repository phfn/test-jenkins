

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                ls
                echo 'build'>builded.txt
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

