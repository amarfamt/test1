node {
  stage('SCM') {
    git 'https://github.com/amarfamt/test1.git'
  }
  stage('sonarqube') {
    
      sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar'
    }
  }

