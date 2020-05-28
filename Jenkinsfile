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
		 if(env.JOB_NAME.contains("qa")){
                echo 'I will execute on qa'
		 } else if (env.JOB_NAME.contains("dev")) {
                echo 'I execute on dev'
              }
			       }
		      }
      }
    }
    }
