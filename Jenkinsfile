pipeline{
    //Directives
    agent any
   node {
  stage('SCM') {
    git 'https://github.com/amarfamt/test1.git'
  }

    stages {
      

        // Stage2 : Testing
        stage ('Test'){
            steps {
                echo ' testing......'

            }
        

        // Stage3 : Publish the source code to Sonarqube
        stage ('Sonarqube Analysis'){
            steps {
                echo ' Source code published to Sonarqube for SCA......'
                withSonarQubeEnv('sonarqube'){ // You can override the credential to be used
                     sh 'mvn sonar:sonar'
                }

            }
        }

        
        
    }

}
