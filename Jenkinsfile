pipeline {
  agent { label 'sonar-node' }
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    stage('Scan') {
      steps {
        withSonarQubeEnv('sonar-server') {
          sh 'mvn clean package sonar:sonar'
      }
    }
  }
}
}
