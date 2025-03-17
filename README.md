# pipeline2
this is pipeline2 repo

pipeline {
    agent any
    stages {
        stage('Check if Jenkinsfile exists') {
            steps {
                script {
                    // Check if Jenkinsfile exists in the root directory
                    if (fileExists('Jenkinsfile')) {
                        echo "Jenkinsfile exists"
                    } else {
                        error "Jenkinsfile does not exist"
                    }
                }
            }
        }
    }
}
