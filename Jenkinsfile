pipeline {
    agent any
    
    environment {
        
        AWS_ACCOUNT_ID=”678330281393”
        AWS_DEFAULT_REGION=”ap-northeast-1”
        IMAGE_REPO_NAME=”repo1”
        IMAGE_TAG=”latest"
        REPOSITORY_URl = “public.ecr.aws/o0a3t4h3/repo1”
}
    
 stages{
  stage{
      script{
     sh "aws ecr-public get-login-password --region ap-northeast-1| docker login --username AWS --password public.ecr.aws/o0a3t4h3/repo1"
    
}
}
 }
}
    
        
