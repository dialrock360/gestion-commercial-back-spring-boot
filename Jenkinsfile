pipeline {
    agent any

    stages {
        
        stage('Clean'){
            steps{
                cleanWs()
            }
        }
        
        stage('Source') {
            steps{
                git(
                        url: 'https://github.com/dialrock360/gestion-commercial-back-spring-boot.git',
                        credentialsId: 'ISIS_HELP_CREDENTIALS',
                        branch: 'master'
                    ) 
            }
        }
        
        stage('Test Unitaire'){
            steps{
                bat 'mvn test'
            }
        }
        
        stage('Test Sonar'){
            steps{
                bat 'mvn sonar:sonar'
            }
        }
        
    }
    

}
