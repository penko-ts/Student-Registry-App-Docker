pipeline {
   agent any
   stages {
      stage('NPM install') {
         steps {
            sh 'npm install'
            }
      }
       parallel {
       stage('Run npm audit tests') {
         steps {
            sh 'npm audit'
            }
          }
        stage('Execute test') {
         steps {
            sh 'npm run test'
            }     
          } 
       }
    }
}     
   
  
   

