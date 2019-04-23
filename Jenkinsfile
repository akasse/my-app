pipeline {
    def mvnHome = tool name: 'Maven', type: 'maven'
    agent any
    stages {
        stage('---clean---') {
            steps {
                sh "${mvnHome}/bin/mvn clean"
            }
        }
        stage('--test--') {
            steps {
                sh "${mvnHome}/bin/mvn test"
            }
        }
        stage('--package--') {
            steps {
                sh "${mvnHome}/bin/mvn package"
            }
        }
    }
}
