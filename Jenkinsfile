@Library("mylibrary")_
pipeline
{
    agent any
    stages
    {
        stage('contdown')
        {
            steps
            {
                script
                {
                    cicd.newgit('https://github.com/Rumana000/mavenp.git')
                }
                
            }
        }
        stage('contbuild')
        {
            steps
            {
                script
                {
                    cicd.maven()
                }
                
            }
        }
        stage('contdeploy')
        {
            steps
            {
                script
                {
                    cicd.newdeploy("${env.JOB_NAME}","172.31.21.41","testapp")
                }
                
            }
        }
        stage('conttest')
        {
            steps
            {
                script
                {
                    cicd.newgit("https://github.com/Rumana000/FunctionalTesting.git")
                    cicd.selenium("${env.JOB_NAME}")
                }
                
            }
        }
        stage('contdelivery')
        {
            steps
            {
                script
                {
                    cicd.newdeploy("${env.JOB_NAME}","172.31.20.194","prodapp")
                }
                
            }
        }
    }
    
    
}
