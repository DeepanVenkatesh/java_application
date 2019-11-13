pipeline {
    agent any
    stages {
        stage('Build') { 
             steps {
                sh 'mvn clean package'
        }
        }
         stage('push to jfrog') { 
             steps {
                rtUpload (
                serverId: 'JFrog_Deepan',
                spec: '''{
                    "files": [
                {
                "pattern": "target/*.war",
                "target": "java_deepan/"
                }
         ]
    }''',
                )
                }
        }
        }
        
    }
