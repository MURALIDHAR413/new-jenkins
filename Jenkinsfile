pipeline{
    agent {
        label 'app-slave'
    }
    environment{
        Deploy = 'stagging'
    }    stages{
        stage('Build'){
            steps{
                echo 'Hello build'            }

        }
        stage('deploy'){
            when{
                allOf{
                   branch 'stagging'
                   environment name: 'Deploy', value: 'stagging'

                }
            } 
            steps{
                echo 'Deploying to production or staging environment'
            }       }
    }
}
