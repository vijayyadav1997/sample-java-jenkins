pipeline{
	/*environment {
   }*/
	agent any
	tools{
		maven 'maven'
	}
	stages{
		stage('build'){
			steps{
				sh 'mvn clean compile package'
			}
		}
    stage('check'){
			steps{
         script {
		 if ($environment == 'qa') {
                echo 'I will execute on qa'
              } else if ($environment == 'dev') {
                echo 'I execute on dev'
              }
			       }
		      }
      }
    }
    }
