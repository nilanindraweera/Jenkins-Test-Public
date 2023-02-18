CODE_CHANGES = getGitChanges()
pipeline
{
    agent any
    triggers
    {
        pollSCM '*/5 * * * *'
    }
    stages
    {
        stages("Build"){
            {
                expression
                {
                    BRANCH_NAME 'Develop'&& CODE_CHANGES == true
                }
            }
            steps
            {
                echo "Building..."

                echo "Build Completed..."
            }                
        }
        stages("Test"){
            when
            {
                expression
                {
                    BRANCH_NAME 'Develop'|| BRANCH_NAME "Master"
                }
            }
            steps
            {
                echo "Testing..."

                echo "Test Completed..."
            }
        }
        stages("Deploy"){
                echo "Deploying..."

                echo "Deploy Completed..."
        }
    }
}