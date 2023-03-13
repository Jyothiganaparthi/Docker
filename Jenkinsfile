pipeline {
    agent any
    
    environment {
        // set environment variables as needed
        AWS_ACCOUNT_ID=”678330281393”
        AWS_DEFAULT_REGION=”us-east-1”
        IMAGE_REPO_NAME=”repo1”
        IMAGE_TAG=”lates
        REPOSITORY_URI = “public.ecr.aws/o0a3t4h3/repo1”
}
    
 stages{
  stage{
      script{
     sh "aws ecr-public get-login-password --region us-east-1 | docker login --username AWS --password-stdin public.ecr.aws/o0a3t4h3/repo1"
    
}
}
 }
}
    
        
