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

        step{
          withMaven(maven : 'Maven'){
           sh 'mvn test'
          }
         }
        }
          stage ('deployment stage') {

        step{
          withMaven(maven : 'Maven'){
           sh 'mvn deploy'
          }
         }
        }
     }
   }
