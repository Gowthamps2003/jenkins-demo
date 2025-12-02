pipeline {
    agent any
        
    stages {
        stage('Test') {
            steps {
                echo "Running build and sending test mail"
            }
        }
    }

    post {
        success {
            emailext (
                to: "gowthamps2003@gmail.com",
                subject: "Build Success",
                body: "Build URL: ${BUILD_URL}"
            )
        }

        failure {
            emailext (
                to: "gowthamps2003@gmail.com",
                subject: "Build FAILED",
                body: "Build URL: ${BUILD_URL}"
            )
        }
    }
}
