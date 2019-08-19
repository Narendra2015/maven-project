pipeline{
   agent any
      stages{
        stage ('compile stage'){

         steps{
            withMaven(maven : 'Maven') {
              sh 'mvn clean compile'
             }
         }
       }
       stage ('Testing stage') {

        steps{
          withMaven(maven : 'Maven'){
           sh 'mvn test'
          }
         }
        }
          stage ('deployment stage') {
           steps{
            withMaven(maven : 'Maven'){
             sh 'mvn deploy'
          }
         }
        }
     }
   }
