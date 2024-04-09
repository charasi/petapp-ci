pipeline {
  agent { label 'sonar-node' }
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    stage('Scan') {
      steps {
        withSonarQubeEnv(installationName: 'sonar-server') {
          sh 'mvn clean sonar:sonar'
          sh './mvnw clear org.sonarsource.scanner.maven:sonar-maven-plugin:3.11.0.3922:sonar'
      }
    }
  }
}
}
