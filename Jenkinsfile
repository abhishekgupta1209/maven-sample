node {
  stage('SCM') {
    checkout scm
  }
 stage('SonarQube analysis') {
    withSonarQubeEnv(credentialsId: '5f2336994187196746811ceed59beb313c2c99de', installationName: 'My SonarQube Server') { // You can override the credential to be used
      bat 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar'
    }
  }
}
