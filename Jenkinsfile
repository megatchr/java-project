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
        stage('Deploy') {
            steps {
             sh 'aws s3 cp ${WORKSPACE}/dist/rectangle-${BUILD_NUMBER}.jar s3://ameg9454-hw10/rectangle-${BUILD_NUMBER}.jar'
            }
        }
        stage('Report'){
            steps{
             sh 'aws cloudformation describe-stack-resources --region us-east-1 --stack-name jenkins'
            }
        }
    }

}
