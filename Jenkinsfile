pipeline {
    agent any
	
	tools {
    maven 'Apache Maven'
  }

    stages {
		
        stage ('Build Stage') {

            steps {
		   
			dir("/var/lib/jenkins/workspace/pipeline"){
			sh 'mvn clean install'
            }
            }
        }

        
		stage ('Deployment Stage') {

            steps {
                
                    sh 'cp /var/lib/jenkins/workspace/pipeline/target/simple-web-app.war /opt/apache-tomcat-8.5.35/webapps '
              
            }
        }


        
    }
}
