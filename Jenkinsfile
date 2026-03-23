pipeline{
    agent {
        label 'app-slave'
    }
    stages{
        stage('Build'){
            steps{
                echo 'Hello build'            }

        }
        stage('deploy'){
            when{
                expression{
                    BRANCH_NAME ==~ /(production|staging)/
                }
            } 
            steps{
                echo 'Deploying to production or staging environment'
            }       }
    }
}
