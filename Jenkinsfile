node
{
    
    stage('scm checkout')
    {
        
     git 'https://github.com/Hemakumar211/manu.git'  
        
    } 
    stage('build stage')
    {
       def mvnhome = tool name: 'Apache Maven 3.6.0', type: 'apache-maven'
       sh "${mvnhome}/bin/mvn package"
        
    }
    stage('sonarqube analysis'){
        
        def mvnhome = tool name: 'Apache Maven 3.6.0', type: 'apache-maven'
        withSonarQubeEnv('sonarqube-7.7'){
        sh "${mvnhome}/bin/mvn sonar:sonar"
        }
    }
    
    
}
  


