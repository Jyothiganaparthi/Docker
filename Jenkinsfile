node{
  stage('build'){
    sh 'printenv'
  }
  stage('dockerlogin'){
    withEnv (["AWS_ACCESS_KEY_ID-${env.AWS_ACCESS_KEY_ID}", "AWS_SECRET_ACCESS_KEY-${env.AWS_SECRET_ACCESS_KEY}", "AWS_DEFAULT_REGION-${env.AWS_DEFAULT_REGION}"]){
         sh 'docker login -u AWS -p $(aws ecr-public get-login-password --region us-east-1) public.ecr.aws/o0a3t4h3'
    }

    }
    
  }
        
