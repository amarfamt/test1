node {
  stage('SCM') {
    git 'https://github.com/amarfamt/test1.git'
  }
  stage('sonarqube') {
    
      sh 'mvn sonar:sonar'
    }
  }

