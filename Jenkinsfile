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
        stage ('Test') {
            steps {
                sh 'make check || true'
                junit '**/target/*.xml'
            }
        }
    }
}















