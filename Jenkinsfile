pipeline{
    agent any
    stages{
        
        stage("Sonar Checks"){
            agent {
                docker {
                    image 'openjdk:11'
                }
            }
            steps{
                script{
                withSonarQubeEnv(credentialsId: 'sonar-token') {
                sh 'chmod gradlew'
                sh './gradlwe sonarqube'
                 }

                }
                
            }
            
        }
    }
   
}