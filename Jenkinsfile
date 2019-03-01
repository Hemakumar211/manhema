node {
  stage('scm checkout'){
        git 'https://github.com/Hemakumar211/manu.git'
        }
   stage('compile-package')
      {
      def mvnhome = tool name: 'Apache Maven 3.5.4', type: 'maven'
        sh "${mvnhome}/bin/mvn package"   
      }
  stage('email notification'){
  mail bcc: '', body: '''hi welcome to jenkins email alerts
  thanks
  hemakumar''', cc: '', from: '', replyTo: '', subject: 'Jenkinsjob', to: 'khema0211@gmail.com'
  
  }

}
