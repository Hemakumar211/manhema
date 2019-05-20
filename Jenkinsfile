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
    
    
}
  stage('email notification'){
  mail bcc: '', body: '''hi welcome to jenkins email alerts
  thanks
  hemakumar''', cc: '', from: '', replyTo: '', subject: 'Jenkinsjob', to: 'khema0211@gmail.com'
  
  }

}
