node {
    def mvnHome = tool name: 'Maven', type: 'maven'
    
    stage('---SCM Checkout---') {
             git 'https://github.com/akasse/my-app'
        }
        stage('---clean---') {
            def mvn = ${mvnHome}/bin/mvn
             sh "${mvn} clean"
        }
        stage('--test--') {
            def mvn = ${mvnHome}/bin/mvn
           sh "${mvn} test"
        }
        stage('--package--') {
            def mvn = ${mvnHome}/bin/mvn
           sh "${mvn} package"
        }
}
