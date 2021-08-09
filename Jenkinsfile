pipeline {
    agent any
    tools {
        maven "maven-test"
    }
    stages {
        stage('Building Maven Project') {
            steps {
                sh "mvn clean package"
            }
        }
    }
}
