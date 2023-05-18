@Library('abcd') _

pipeline{
	agent any
      stages{
           stage('Checkout'){
	    
               steps{
                   sh 'echo ${env.gitlabSourceBranch} '
                   code('${env.gitlabSourceBranch}','https://github.com/Athulkrishnaur/DevOpsClassCodes.git')
                   //git("https://github.com/Athulkrishnaur/DevOpsClassCodes.git")
              }
          }
          stage('Compile'){
             
              steps{
                  echo 'compiling..'
                  sh 'ls'
	      }
          }
          stage('CodeReview'){
		  
              steps{
		    
		  echo 'codeReview'
                  sh 'mvn pmd:pmd'
              }
          }
           stage('UnitTest'){
		  
              steps{
	         
                  sh 'mvn test'
	      }
          }
          
          stage('Package'){
		  
              steps{
		  
                  sh 'mvn package'
              }
          }
	     
          
      }
}
