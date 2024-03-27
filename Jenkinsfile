pipeline {
  agent{label "windows"}
  stages{
   stage('Hello'){
    steps{
     echo "hello again from Jenkinsfile"
    }
   }
   stage('for the fix branch'){
     when{
        branch "fix-*"
     }
     steps {
       sh '''
       	  cat README.d
       '''  
     }
   }
   stage('for the PR'){
    when{
       branch 'PR-*'
    }
    steps{
    	echo 'this only runs for the PRs'
    }
   }
 }
}
