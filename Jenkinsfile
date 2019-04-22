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
             sh 'ls ${WORKSPACE}/dist/rectangle-${BUILD_NUMBER}.jar'
             sh 'aws'
            }
        }
    }

}
