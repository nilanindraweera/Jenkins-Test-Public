//CODE_CHANGES = getGitChanges()
pipeline
{
    agent any
    triggers
    {
        pollSCM '*/5 * * * *'
    }
    stages
    {
        stage("Build"){
            when
            {
                expression
                {
                    BRANCH_NAME == 'Develop'//&& CODE_CHANGES == true
                }
            }
            steps
            {
                echo "Building..."

                echo "Build Completed..."
            }                
        }
        stage("Test"){
            when
            {
                expression
                {
                    BRANCH_NAME == 'Develop' || BRANCH_NAME == "Master"
                }
            }
            steps
            {
                echo "Testing..."

                echo "Test Completed..."
            }
        }
        stage("Deploy"){
            steps
            {
                echo "Deploying..."

                echo "Deploy Completed..."
            }
        }
    }
}