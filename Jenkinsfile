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
        stage("Deploying"){
            script {
                input message: 'Approve deployment?', ok: 'Deploy To Production'
                    echo 'Deploying'
                }
        }
    }
}