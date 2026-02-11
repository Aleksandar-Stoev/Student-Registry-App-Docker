pipeline{
    agent{
        label any
    }
    stages{
        stage("Install Dependencies"){
            steps{
                bat "npm install"
            }
        stage("Run UI Tests"){
            steps{
                bat "npm test"
            }
        }
    }
}
