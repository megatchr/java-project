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
                sh 'aws --v'
             sh 'aws s3 cp ${WORKSPACE}/dist/rectangle-${BUILD_NUMBER}.jar s3://ameg9454-hw10/rectangle-${BUILD_NUMBER}.jar'
          
            }
        }
    }

}
