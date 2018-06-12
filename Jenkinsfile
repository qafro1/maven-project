pipeline {
    agent any
    tools {
        maven: 'localmaven'
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















