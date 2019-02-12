pipeline{
    agent any
   tools{
   maven 'Apache Maven 3.5.4'
   }
stages {
    stage('scm checkout')
    {
    git 'https://github.com/Hemakumar211/manu'
    }
    stage('compile package')
    {
    
        sh 'mvn package'
    }
}
}
