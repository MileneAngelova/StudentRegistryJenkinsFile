pipeline{
    agent any
    stages{
        stage("NPM Install"){
            steps{
                bat 'npm install'
            }
        }
       stage("Run Integration tests"){
          steps{
            bat 'npm test'
         }
        }
        stage("Deploy to Staging"){
           steps {
             echo 'Deploying to Stage...'
            }
        }
        stage("Approval for Production Deploy"){
            steps {
             input message: 'Approve Deploy'
            }
        }
         stage("Deploy to Production"){
            steps {
                echo 'Deploying to Production...'
            }
        }
    }
}