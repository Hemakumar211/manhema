node {
    stage('scm checkout')
    {
    git 'https://github.com/Hemakumar211/manu'
    }
    stage('compile package')
    {
     def mvnhome = tool name: 'Apache Maven 3.5.4', type: 'maven'
        sh "${mvnhome}/bin/mvn package"
    }
}

