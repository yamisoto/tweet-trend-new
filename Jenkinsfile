pipeline {
    agent {
        node {
            label 'maven'
        }
    }
    environment {
        PATH = "/opt/apache-maven-3.9.2/bin:$PATH"
        REGISTRY = 'https://valaxy05.jfrog.io'
    }
    stages {
        stage("Prepare") {
            steps {
                script {
                    // Ensure there are executable commands here
                }
            }
        }
        // Other stages...
    }
    post {
        always {
            echo 'This will always execute.'
        }
        success {
            echo 'Build and Test stages succeeded.'
        }
        failure {
            echo 'Build or Test stages failed.'
        }
    }
}
