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
            if (env.JOB_NAME == 'test-pipeline-qa') {
                echo 'I will execute on qa'
              } else if (env.JOB_NAME == 'test-pipeline') {
                echo 'I execute on dev'
              }
			       }
		      }
      }
    }
    }
