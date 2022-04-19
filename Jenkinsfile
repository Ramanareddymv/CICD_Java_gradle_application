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
<<<<<<< HEAD
               withSonarQubeEnv(installationName: 'sonar', credentialsId: 'sonar-tocken') {
=======
               withSonarQubeEnv(credentialsId: 'sonar-tocken') {
>>>>>>> 9cb7237d46af838cbd4b76ef5b61a3b941398a01
                     sh 'chmod +x gradlew'
                     sh './gradlew sonarqube'
                }
            }
            }
            
        }
    }
   
