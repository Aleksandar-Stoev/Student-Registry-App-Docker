pipeline{
    agent any
    
    stages{
        stage("Install Dependencies"){
            steps{
                bat "npm install"
            }
        }
        stage("Testing"){
            failFast true
            parallel{
                stage("Run npm security"){
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
        stage("Approval for Deployment"){
            steps{
                input message: "Do you want to deploy the application?",
                    ok: "Deploy"
            }
        }
        stage("Deploy"){
            steps{
                echo "Deploying application..."
            }
        }
    }
}
