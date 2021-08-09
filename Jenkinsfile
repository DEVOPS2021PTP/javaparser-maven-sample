pipeline {
    agent any
    tools {
        maven "maven-test"
	jdk "Chalapathi"
    }
    stages {
        stage('Building Maven Project') {
            steps {
                git 'https://github.com/Chala9228/javaparser-maven-sample.git'
                sh "mvn clean package"
            }
        }
    }
}
