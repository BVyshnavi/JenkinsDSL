node {
  echo "current build number: ${currentBuild.number}"
  stage('SonarQube analysis') {
    def scannerHome = tool 'Sonarqube Scanner';
    withSonarQubeEnv('sonarqube') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
