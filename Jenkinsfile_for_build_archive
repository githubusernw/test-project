pipeline{
    agent any
    stages {
        stage ('Build') {
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo 'new archiving'
                    archiveArtifacts artifacts: '**/*.war'
                }
            }

        }
        
    }
}