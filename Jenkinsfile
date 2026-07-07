=======Jenkinsfile==============

pipeline {
    agent {
        label 'linux-agent'
    }
    
    stages {
        stage ('stage 1 - checkout') {
            steps {
                echo "Running on node: ${env.NODE_NAME}"
                echo "Checking out source code....."
            }
        }
        stage ('stge 2 - Build') {
            steps {
                sh '''
                    echo "Building an application......"
                    pwd
                    ls -l 
                '''
            }
        }
        stage ('stage 3 - Test') {
            steps {
                sh '''
                    echo "Running tests....."
                    echo "All tests passed."
                '''
            }
        }
    }
    post {
        always {
            echo "Pipeline execution completed"
        }
        
        success {
            echo "Pipeline execution successfully."
        }
        
        failure {
            echo "Pipeline execution failed"
        }
    }
}
