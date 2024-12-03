
pipeline {
    agent any
    environment {
        MAVEN_HOME = '/etc/maven'  // Set this to your actual Maven installation path
        PATH = "${MAVEN_HOME}/bin:${/usr/share/apache-maven}" // Update PATH
    
    
    stages {
        stage('git checkout') {
            steps {
                git credentialsId: 'jenkinspassword', url: 'https://github.com/DeviSriKannan/CI_CD_Integration.git'
            }
        }
        stage('mvn build') {
            steps {
                mvnHome=tool 'maven-3.2.5'
                sh "${mvnHome}/bin/mvn --version"
                sh "${mvnHome}/bin/mvn clean test surefire-report:report"
            }
        }
    
    }
}
