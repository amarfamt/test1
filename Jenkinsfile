pipeline{
    //Directives
    agent any
    tools {
        maven 'maven'
    }

    stages {
        // Specify various stage with in stages

        // stage 1. Build
        stage ('Build'){
            steps {
                sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar'
            }
        }

        // Stage2 : Testing
        stage ('Test'){
            steps {
                echo ' testing......'

            }
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
