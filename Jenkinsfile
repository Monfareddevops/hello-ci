pipeline {
    agent any
    stages {
        stage('Preparation') {
            steps {
                echo 'Cloning source...'
                checkout scm
            }
        }
        stage('Run Script') {
            steps {
                sh 'chmod +x hello.sh && ./hello.sh'
            }
        }
        stage('Archive') {
            steps {
                sh 'tar -czf output.tar.gz hello.sh'
                archiveArtifacts artifacts: 'output.tar.gz'
            }
        }
    }
}
