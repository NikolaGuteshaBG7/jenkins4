/*
basic pipeline for npm front end backend application
*/
pipeline
{
    agent any
    stages
    {                
        stage("Package Installation")// installing all npm necessary packages
        {
            steps
            {                
                echo "Installing npm packages"
                nodejs('Node16.2.0')
                {
                    sh 'npm install'
                }
            }
        }                
        stage("Build Front End")
        {
            steps
            {                
                echo "Building FE part"
                nodejs('Node16.2.0')
                {
                    sh 'npm run build'
                }
            }
        }
        stage("Start applcation")
        {
            steps
            {                
                echo "Starting Application"
                nodejs('Node16.2.0')
                {
                    sh 'npm start'
                }
            }
        }
    }

}
