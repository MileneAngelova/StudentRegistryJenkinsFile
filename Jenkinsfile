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
            steps {
                echo 'Deploying'
                }
        }
    }
}