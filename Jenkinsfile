pipeline{
    agent any
    
    stages{
        stage("Install Dependencies"){
            steps{
                bat "npm install"
            }
        }
        stage(Run npm security){
            steps{
                bat "npm audit"
            }
        }
        stage("Run UI Tests"){
            steps{
                bat "npm test"
            }
        }
    }
}
