pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'make' (1)
                archiveArtifacts artifacts: '**/target/*.war', fingerprint: true (2)
            }
        }
    }
}

#pipeline {
#    agent any
#    stages{
#      stage('Build'){
#
#         steps{
#             sh 'mvn clean package'
#               
#           }
#      }
#   }
#}
