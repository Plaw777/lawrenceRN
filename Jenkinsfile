pipeline{
    tools{
        jdk 'myjava'
        maven 'mymaven'
    }
	agent any
      stages{
           stage('Checkout with slave1'){
              steps{
		 echo 'cloning..'
                 git 'https://github.com/Plaw777/lawrenceRN.git'
              }
          }
          stage('Compile with slave2'){
              steps{
                  echo 'compiling..'
                  sh 'mvn compile'
	      }
          }
          stage('CodeReview with slave1'){
              steps{
		    
		  echo 'codeReview'
                  sh 'mvn pmd:pmd'
              }
          }
          
          stage('Package with Master'){
              steps{
                  sh 'mvn package'
              }
          }
      }
}
