pipeline {
    agent any
    environment {
        AWS_ACCOUNT_ID=”678330281393”
        AWS_DEFAULT_REGION=”ap-northeast-1”
        IMAGE_REPO_NAME=”repo1”
        IMAGE_TAG=”v1"
        REPOSITORY_URl = “678330281393.dkr.ecr.ap-northeast-1.amazonaws.com/repo1”
    }
     stages {
        
         stage('Logging into AWS ECR') {
            steps {
                script {
                sh """aws ecr get-login-password --region ${AWS_DEFAULT_REGION} | docker login --username AWS --password-stdin ${AWS_ACCOUNT_ID}.dkr.ecr.${AWS_DEFAULT_REGION}.amazonaws.com"""
                }
            }
         }
     }

}
    
        
