pipeline{
    agent any
    stages{
        stage("sonar quality check"){
            steps{
               withSonarQubeEnv(installationName: 'sonar', credentialsId: 'sonar-token') {
                     sh 'chmod +x gradlew'
                     sh './gradlew sonarqube'
                }
            }
            }
            
        }
    }
   
