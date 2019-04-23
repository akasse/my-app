node {
    
    stage('---SCM Checkout---') {
             git 'https://github.com/akasse/my-app'
        }
        stage('---clean---') {
            def mvnHome = tool name: 'Maven', type: 'maven'
             sh "${mvnHome}/bin/mvn clean"
        }
        stage('--test--') {
            def mvnHome = tool name: 'Maven', type: 'maven'
           sh "${mvnHome}/bin/mvn test"
        }
        stage('--package--') {
            def mvnHome = tool name: 'Maven', type: 'maven'
           sh "${mvnHome}/bin/mvn package"
        }
}
