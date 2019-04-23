node {
    
    
    stage('---SCM Checkout---') {
             git 'https://github.com/akasse/my-app'
        }
        stage('---clean---') {
            def mvnHome = tool name: 'Maven', type: 'maven'
            def mvn = ${mvnHome}/bin/mvn
             sh "${mvn} clean"
        }
        stage('--test--') {
            def mvnHome = tool name: 'Maven', type: 'maven'
            def mvn = ${mvnHome}/bin/mvn
           sh "${mvn} test"
        }
        stage('--package--') {
            def mvnHome = tool name: 'Maven', type: 'maven'
            def mvn = ${mvnHome}/bin/mvn
           sh "${mvn} package"
        }
}
