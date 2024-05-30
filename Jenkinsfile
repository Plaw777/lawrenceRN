pipeline{
    tools{
        jdk 'plawjava'
        maven 'plawmaven'
    }
	agent any
      stages{
           stage('Checkout with git'){
              steps{
		 echo 'cloning repository..'
                 git 'https://github.com/Plaw777/lawrenceRN.git'
              }
          }
          stage('Compile with maven'){
              steps{
                  echo 'high level language to machine language..'
                  sh 'mvn compile' 
	      }
          }
          stage('CodeReview with maven'){
              steps{
		    
		  echo 'Programming Mistakes And Vulnerabilities'
                  sh 'mvn pmd:pmd'
              }
          }
          
          stage('Package'){
              steps{
                  sh 'mvn package'
              }
          }
      }
}
