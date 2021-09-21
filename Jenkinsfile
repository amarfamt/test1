node {
  stage('SCM') {
    git 'https://github.com/foo/foo.git'
  }
  stage('sonarqube') {
     { // You can override the credential to be used
      sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar'
    }
  }
}
