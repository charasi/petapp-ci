pipeline {
  agent { label 'sonar-node' }
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stage("Compile"){
            steps{
                sh "mvn clean compile"
            }
        }
        
         stage("Test"){
            steps{
                sh "mvn test"
            }
        }
}
