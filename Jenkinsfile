pipeline {
    agent any

    tools {
        maven 'localMaven'
    }
    
    stages {
        stage ('Build') {
            steps {
                sh 'mvn clean package'
                archiveArtifacts artifacts: '**/target/*.war'
            }
        }
    }
}















