pipeline {
agent {
label {
		label "built-in"
		customWorkspace "/data/project-myapp"
		
		}
		}
		
	stages {
		
		stage ('CLEAN_OLD_M2') {
			
			steps {
				sh "rm -rf /home/nisha/.m2/repository"
				
			}
			
		}
	
		stage ('MAVEN_BUILD') {
		
			steps {
						
						sh "mvn clean package"
			
			}
			
		
		}
		
		stage ('COPY_WAR_TO_Server'){
		
				steps {
						
						sh "scp -r target/LoginWebApp.war nisha@172.31.36.195:/data/project/wars"

						}
				
				}
	
	
	
	}
		
}
