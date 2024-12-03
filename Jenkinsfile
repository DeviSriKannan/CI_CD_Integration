pipeline {
    agent any
    
    
    stages {
        stage('git checkout') {
            steps {
                git credentialsId: 'jenkinspassword', url: 'https://github.com/DeviSriKannan/CI_CD_Integration.git'
            }
        }
    }
}
