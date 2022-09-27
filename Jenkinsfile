pipeline{
    agent any

    stages{
        stage('code-checkout'){
            steps{
                git url:'https://github.com/hari-edm/spring-petclinic.git', branch:'feature/d-pipeline'
            }
        }
        stage('build'){
            steps{
                sh 'mvn package'
            }
        }
        stage('archive-test-results'){
            steps{
                junit testResults: '**/surefire-reports/*.xml'
            }
        }
    }
}
