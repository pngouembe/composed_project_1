pipeline {
    agent { docker { image 'python:3.10.1-alpine' } }
    triggers{upstream(upstreamProjects: 'My-pipeline', threshold: hudson.model.Result.SUCCESS)}
    stages {
        stage('build') {
            steps {
                sh 'python --version'
                sh 'python test_script.py'
            }
        }
    }
}
