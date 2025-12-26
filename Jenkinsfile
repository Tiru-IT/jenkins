pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo "Building"
            }
        }
        stage('Test') {
            steps {
                echo "Testing"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying"
            }
        }
    }
    post{
        always{
            echo 'I will always say Hello agian!'
        }
        success{
            echo 'i am success'
        }
        failure{
            echo 'i am failure'
        }
    }
}