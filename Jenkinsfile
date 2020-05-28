pipeline{
	
	environment {
		script {
		 if(env.JOB_NAME.contains("qa")){
                echo 'I will execute on qa'
			 deployenvior = "qa"
		 } else if (env.JOB_NAME.contains("dev")) {
                echo 'I execute on dev'
			 deployenvior = "dev"
              }
			       }
   }
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
				echo ${deployenvior}
		      }
      }
    }
    }
