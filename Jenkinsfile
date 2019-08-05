stage('Sonarqube') {
    steps {
        def scannerHome = tool 'SonarScanner 4.0';
        withSonarQubeEnv('sonarqube') {
            sh "${scannerHome}/bin/sonar-scanner"
        }
    }
}
