pipeline {
  agent { label 'sonar-node' }
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    stage('Scan') {
      steps {
        withSonarQubeEnv(installationName: 'sonar-server') {
          sh 'mvn clean compile sonar:sonar'
      }
    }
  }
}
}
