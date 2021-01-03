pipeline{
  agent any
  tools {
      maven 'Maven3.6.3'
      }
  stages {
     stage('SCM Checkout') {
        steps {
             git "https://github.com/saravana-ganesh12/TestApp"
              }
          }
     stage('Compile-package'){
        steps {
            sh "mvn -version"
            sh "mvn clean install"
            sh "mvn package"
            }
         }
  post {
     always {
       cleanWS()
      }
    }
} 
