pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh "echo this is build"
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
            }
        }
    }



post {
    always{
        echo "this section runs always"
    }

    sucess{
        echo "this section runs when pipeline success"
    }
    failure{
        echo "this section runs when pipeline fails"
    }
}
}