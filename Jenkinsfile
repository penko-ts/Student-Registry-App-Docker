pipeline {
    agent any
    stages {
        stage('NPM install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run npm audit tests') {
            parallel {
                stage('Run npm audit') {
                    steps {
                        sh 'npm audit'
                    }
                }
                stage('Execute tests') {
                    steps {
                        sh 'npm run test'
                    }     
                } 
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to Staging'
                // Add staging deployment logic here
            }
        }
        stage('Approval for Production Deployment') {
            steps {
                script {
                    input message: 'Approve deployment to production?', ok: 'Deploy'
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to Production'
                // Add production deployment logic here
            }
        } 
    }
}
