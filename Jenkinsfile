node{
    stage('code-checkout'){
        git url:'https://github.com/hari-edm/spring-petclinic.git', branch: 'feature/s-pipeline'
    }

    stage('build'){
        sh 'mvn package'
    }

    stage('archive-test-results'){
        junit testResults: '**/surefire-reports/*.xml'
    }
}
