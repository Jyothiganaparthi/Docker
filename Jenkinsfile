pipeline {
    agent any
    
    environment {
        // set environment variables as needed
        DOCKER_REGISTRY = "public.ecr.aws/o0a3t4h3/repo1"
        DOCKER_REPO = "repo1"
        DOCKER_TAG = "${env.BUILD_NUMBER}"
    }
 stages{
  stage{
 withCredentials([<object of type com.cloudbees.jenkins.plugins.awscredentials.AmazonWebServicesCredentialsBinding>]) {
    sh 'docker login -u AWS -p (aws ecr-public get-login-password --region us-east-1) public.ecr.aws/o0a3t4h3'
}
}
 }
}
    
        
