node{
  stage('build'){
    sh 'printenv'
  }
  stage('dockerlogin'){
    withEnv (["AWS_ACCESS_KEY_ID-${env.AWS_ACCESS_KEY_ID}","AWS_SECRET_ACCESS_KEY-${env.AWS_SECRET_ACCESS_KEY}","AWS_DEFAULT_REGION-${env.AWS_DEFAULT_REGION}"]){
         sh 'docker login -u AWS -p $(aws ecr get-login-password --region ap-northeast-1) 678330281393.dkr.ecr.ap-northeast-1.amazonaws.com
    }

    }
    
  }
        
