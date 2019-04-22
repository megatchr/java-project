pipeline {
    agent any

    stages {
        stage('Unit Tests'){
            steps{
             sh 'ant -f test.xml -v'
             junit '**/reports/result.xml'
            }
        
        }
        stage('Build') {
            steps {
                  sh 'ant -f build.xml -v'
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
