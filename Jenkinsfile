pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
                // Timeout counter starts BEFORE agent is allocated
                timeout(time: 10, unit: 'SECONDS')
                disableConcurrentBuilds()
                retry(1)
    }
   
    stages {
        stage('Build') {
            steps {
                sh "echo this is build"
                sh "sleep 10"
            }
        }
        stage('Test') {
            steps {
                sh "echo this is test"
            }
        }
        stage('Deploy') {
            steps {
                sh "echo this is deploy"
                error "pipeline failed"
            }
        }
    }



post {
    always{
        echo "this section runs always"
        deleteDir()
    }

    success{
        echo "this section runs when pipeline success"
    }
    failure{
        echo "this section runs when pipeline fails"
    }
}
}