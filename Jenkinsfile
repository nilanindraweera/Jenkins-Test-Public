//CODE_CHANGES = getGitChanges()
pipeline
{
    agent any
    triggers
    {
        pollSCM '*/5 * * * *'
    }
    environment
    {
        NEW_VERSION = "0.0.0.1"
        MY_BRANCH_NAME = "Develop"
    }
    stages
    {
        stage("Build"){
            when
            {
                expression
                {
                    MY_BRANCH_NAME == 'Develop'//&& CODE_CHANGES == true
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
                    MY_BRANCH_NAME == 'Develop' || MY_BRANCH_NAME == "Master"
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