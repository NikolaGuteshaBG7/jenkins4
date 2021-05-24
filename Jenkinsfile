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
        stage("Package audit")// installing all npm necessary packages
        {
            steps
            {                
                echo "Auditing npm packages"
                nodejs('Node16.2.0')
                {
                    sh 'npm audit'
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
        stage("Test")
        {
            steps
            {                
                echo "testing....."
                /*
                nodejs('Node16.2.0')
                {
                    sh 'npm run build'
                }*/
            }
        }


        /*

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
        }*/
    }

}
