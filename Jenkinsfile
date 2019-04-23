node {
    def mvnHome = tool name: 'Maven', type: 'maven'
    def mvn = ${mvnHome}/bin/mvn
    stage('---SCM Checkout---') {
             git 'https://github.com/akasse/my-app'
        }
        stage('---clean---') {
             sh "${mvn} clean"
        }
        stage('--test--') {
           sh "${mvn} test"
        }
        stage('--package--') {
           sh "${mvn} package"
        }
}
