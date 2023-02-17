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
                echo "Building..."

                echo "Build Completed..."
        }
        stages("Test"){
                echo "Testing..."

                echo "Test Completed..."
        }
        stages("Deploy"){
                echo "Deploying..."

                echo "Deploy Completed..."
        }
    }
}