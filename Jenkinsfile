pipeline{
    agent {
        label 'app-slave'
    }
    environment{
        DEPLOY = 'stagging'
    }    
    stages{
        stage('Build'){
            steps{
                echo 'Hello build'
            }
        }

        stage('deploy'){
            when{
                allOf{
                   branch 'stagging'
                   environment name: 'DEPLOY', value: 'stagging'

                }
            } 
            steps{
                echo 'Deploying to production or staging environment'
            }       }
        }
    }

