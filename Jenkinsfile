tools{
 maven 'Apache Maven 3.5.4'
}
node{
    stage('scm checkout')
    {
    git 'https://github.com/Hemakumar211/manu'
    }
    stage('compile package')
    {
    
        sh 'mvn package'
    }
}
