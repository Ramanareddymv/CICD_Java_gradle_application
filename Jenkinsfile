pipeline{
    agent any
    stages{
        stage("sonar quality check"){
            agent {
                docker {
                    image 'openjdk:11'
                }
            }
            steps{
               withSonarQubeEnv(installationName: 'sonar', credentialsId: 'sonar-tocken') {
                     sh 'chmod +x gradlew'
                     sh './gradlew sonarqube'
                }
            }
            }
            
        }
    }
   
