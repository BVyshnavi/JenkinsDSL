node {
  stage('SonarQube analysis') {
    def scannerHome = tool 'Sonarqube Scanner';
    withSonarQubeEnv('sonarqube') {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
