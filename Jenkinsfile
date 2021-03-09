pipeline {
    agent {
        label 'master' 
    }
  
    stages {
        stage('build & SonarQube analysis') {
            steps {
                withSonarQubeEnv(installationName:'Sonar' , credentialsId: 'sonar_secret_new')
                {
                 bat 'mvn clean install sonar:sonar'
                }
            }
        } 
       
    }
}
