pipeline {
 agent any
    stages{
        stage('Build'){
            steps{
               sh 'docker build -t image1 .'
            }
        }
        stage('ecr login'){
            steps{
                withCredentials([[
    $class: 'AmazonWebServicesCredentialsBinding',
    credentialsId: "aws",
    accessKeyVariable: 'AWS_ACCESS_KEY_ID',
    secretKeyVariable: 'AWS_SECRET_ACCESS_KEY'
]]) {
    sh 'aws ecr get-login-password --region ap-northeast-1 | docker login --username AWS --password-stdin 678330281393.dkr.ecr.ap-northeast-1.amazonaws.com'
                    sh 'docker tag image1:latest 678330281393.dkr.ecr.ap-northeast-1.amazonaws.com/image1:latest'
                    sh 'docker push 678330281393.dkr.ecr.ap-northeast-1.amazonaws.com/image1:latest'
}
   }
        }
    }
}
    
        
