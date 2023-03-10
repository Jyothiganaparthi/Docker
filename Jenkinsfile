node{
 
  
  stage('dockerlogin'){
    withCredentials([[
    $class: 'AmazonWebServicesCredentialsBinding',
    credentialsId: "AKIAZ335CVWYZWQ6SQQK (aws-credentials)",
    accessKeyVariable: 'AWS_ACCESS_KEY_ID',
    secretKeyVariable: 'AWS_SECRET_ACCESS_KEY'
]]) {
    

         sh 'docker login -u AWS -p $(aws ecr-public get-login-password --region us-east-1) public.ecr.aws/o0a3t4h3'
    }

    }
    
  }
        
