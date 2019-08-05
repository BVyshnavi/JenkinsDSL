node {
  sonarqube {
    properties {
      property "sonar.host.url", "http://internal-sonarqube-sonarelb-1fc7si6vyhwcw-1688826945.us-east-1.elb.amazonaws.com/sonar"
      property "sonar.projectKey", "4d3f01c986f1aae48e1905f0d090a45adaba6e63"
      property "sonar.projectName", "sonarqube"
    }
  }
  
  stage('SonarQube analysis') {
    def scannerHome = tool 'Sonarqube Scanner';
    withSonarQubeEnv('sonarqube') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
