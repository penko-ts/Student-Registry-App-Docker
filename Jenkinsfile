pipeline {
   agent any
   stages {
      stage('NPM install') {
         steps {
            sh 'npm install'
            }
         }      
       stage('Execute test') {
         steps {
            sh 'npm run test'
            } 
          } 
       }
}     
   
  
   

