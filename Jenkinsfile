pipeline{
	environment {
		deployenvior=deployenviornment()	
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
				echo "${deployenvior}"
		     }
		}
		
		if(${deployenvior} == 'qa'){
		stage('check'){
			steps{
				echo "${deployenvior}"
		     }
		}
		}
		
	}
	
}
	
	def deployenviornment(){
		script {
		 if(env.JOB_NAME.contains("-qa")){
                echo 'I will execute on qa'
			 return "qa"
		} else if (env.JOB_NAME.contains("dev")) {
                echo 'I execute on dev'
			 return "dev"
        }
		}
	}
