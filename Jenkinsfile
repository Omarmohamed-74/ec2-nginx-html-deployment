node{
  git branch: 'main', url: 'https://github.com/Omarmohamed-74/ec2-nginx-html-deployment.git'
  stage('buld'){
    try{
    sh 'echo "building stage"'
    }
    catch(Exception e){
      sh'echo "exception found"
      throw e
    }
  } 
  stage('test'){
     if (env.BRANCH_NAME == "feat"){
        sh 'echo "testing stage"'
      }
      else{
        sh 'echo "skipping testing stage"'
     }
  }
}
