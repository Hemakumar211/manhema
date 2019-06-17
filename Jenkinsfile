node
{
    
    stage('scm checkout')
    {
        
     git 'https://github.com/Hemakumar211/manu.git'  
        
    } 
    stage('build stage')
    {
       def mvnhome = tool name: 'apache-maven-3.6.0', type: 'maven'
       sh "${mvnhome}/bin/mvn package"
        
    }
    stage('sonarqube analysis'){
        
        def mvnhome = tool name: 'apache-maven-3.6.0', type: 'maven'
        withSonarQubeEnv('sonarqube-7.7'){
        sh "${mvnhome}/bin/mvn sonar:sonar"
        }
    }
    stage('deployment stage){
          
          sh 'cp /var/lib/jenkins/workspace/pipeline-project/target/*.war /opt/apache-tomcat-8.5.41/webapps/'
          
          }
    
    
}
  

}
