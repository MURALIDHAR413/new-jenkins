pipeline{
    agent{
        label 'app-slave'
    }
    stages{
        stage('Docker'){
            steps{
                sh 'docker --version'
            }
        }
    }
}
