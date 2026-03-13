pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Hi"
                sh 'hostname -i'
            }
        }
        stage('Test') {
            agent{
                label 'app-slave'
            }
                 steps {
                                echo "laddu"
                     sh 'hostname -i'

            }
            
           
        }
        stage('Deploy') {
            steps {
                                echo "deploy"

            }
        }
    }
}
