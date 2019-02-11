pipeline {
    agent any
    tools {
    maven 'Apache Maven 3.5.4'
  }
    stages {
		
        stage ('Build Stage') {

            steps {
			dir("/var/lib/jenkins/workspace/pipeline"){
			sh 'mvn clean package'
            }
            }
        }

        
		stage ('Deployment Stage') {

            steps {
                
                    sh 'cp /var/lib/jenkins/workspace/pipeline/target/simple-web-app.war /opt/apache-tomcat-8.5.37/webapps/'
              
            }
        }


        
    }
}
