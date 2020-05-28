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
            if (env.BRANCH_NAME == 'master') {
                echo 'I will execute on dev'
              } else {
                echo 'I execute on qa'
              }
			       }
		      }
      }
    }
    }
