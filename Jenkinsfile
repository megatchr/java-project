pipeline {
    agent any

    stages {
        stage('Unit Tests'){
            steps{
             sh 'ant -f test.xml -v'
            }
        
        }
        stage('Build') {
            steps {
                echo 'Building src..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
