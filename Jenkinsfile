pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'build' (1)
                archiveArtifacts artifacts: '**/target/*.war', fingerprint: true (2)
            }
        }
    }
}

