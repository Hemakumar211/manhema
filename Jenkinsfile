pipeline {
    agent any

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
                
                    sh 'cp /root/.jenkins/workspace/abc/target/simple-web-app.war /opt/apache-tomcat-8.5.34/webapps '
              
            }
        }


        
    }
}
