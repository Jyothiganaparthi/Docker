pipeline {
agent any
environment {
AWS_ACCOUNT_ID=”678330281393”
AWS_DEFAULT_REGION=”ap-northeast-1”
IMAGE_REPO_NAME=”repo1”
IMAGE_TAG=”v1”
REPOSITORY_URI = “${AWS_ACCOUNT_ID}.dkr.ecr.${AWS_DEFAULT_REGION}.amazonaws.com/${IMAGE_REPO_NAME}”
}

stages {

stage(‘Logging into AWS ECR’) {
steps {
script {
sh “aws ecr get-login-password — region ${AWS_DEFAULT_REGION} | docker login — username AWS — password-stdin ${AWS_ACCOUNT_ID}.dkr.ecr.${AWS_DEFAULT_REGION}.amazonaws.com”
}
}
}
}
    stage(‘Cloning Git’) {
steps {
 checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'git', url: 'https://github.com/Jyothiganaparthi/Docker.git']])
}
}
}
    
        
