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
        stage("if condtion"){
            if(env.BRANCH_NAME=='main'){
                echo "Hello main branch"
            }
            else{
                echo "Hello from ${env.BRANCH_NAME}"
            }
        }
            
            
        }
    }
   
