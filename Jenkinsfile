pipeline {
    agent any
    stages {
        stage('Build') { 
             steps {
                sh 'mvn clean package'
        }
        }
        stage('SonarQube analysis') { 
             steps {
                withSonarQubeEnv('Sonar_Deepan') { 
                sh 'mvn sonar:sonar'
                }
        }
        }
        }
        
    }
