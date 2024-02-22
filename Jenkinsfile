pipeline {
    agent {
        node {
            label 'maven'
        }
    }
    environment {
        PATH = "/opt/apache-maven-3.9.2/bin:$PATH"
       
    }
    stages {
        stage("build") {
            steps {
                script {
                    #// Ensure there are executable commands here
                   sh  'mvn clean depoly'
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
