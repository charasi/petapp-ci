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
}
