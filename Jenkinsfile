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
        
    }
    
    
}
