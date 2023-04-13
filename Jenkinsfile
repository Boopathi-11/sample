pipeline 
{
    agent any

    stages 
    {
        stage ('Build')
        {

           steps
           {
               checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'bd27d7d6-4216-47be-917c-33ea629a7876', url: 'https://github.com/Boopathi-11/sample.git']])
               echo 'Build App'
           }
        }

        stage ('Deploy')
        {

           steps
           {
                bat 'javac sample.java'
           }
        }

        stage ('Test')
        {

           steps
           {
               bat 'java sample'
               echo 'Deploy App'
           }
        }

    }
}
