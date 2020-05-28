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
            if (env.JOB_NAME == 'test-pipeline') {
                echo 'I will execute on dev'
              } else {
                echo 'I execute on qa'
              }
			       }
		      }
      }
    }
    }
