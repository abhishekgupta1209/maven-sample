node {
  stage('SCM') {
    checkout scm
  }
 stage('SonarQube analysis') {
    withSonarQubeEnv('My SonarQube Server') { // You can override the credential to be used
      bat 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar'
    }
  }
}
