pipeline {
    // pre-build
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        COURSE = "Jenkins"
    }
    
    // build
    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                        echo "Building"
                        echo $COURSE
                        env
                    """
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh """
                        echo "Testing"
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh """
                        echo "Deploying"
                    """
                }
            }
        }
    }
    // post-build
    post {
        always {
            echo 'I will always say Hello agian!'
            cleanWs() // clean the workspace 
        }
        success {
            echo 'i am success'
        }
        failure {
            echo 'i am failure'
        }
    }
}