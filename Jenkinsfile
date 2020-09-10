
pipeline {
    agent any
    stages {
        stage('Git SCM checkout'){
            steps {
                //git branch: '${BRANCH}',
                //    url: 'https://github.com/rahulK299/test123.git' 
                checkout scm: [$class: 'GitSCM', 
                    userRemoteConfigs: [[credentialsId: 'gitlab-acess',url: 'https://github.com/rahulK299/test123.git']], 
                    branches: [[name: '${BRANCH}']]], changelog: false, poll: false
            }
        }
        
        stage('HELLO') {
            steps {
                sh 'echo ${HELLO}'
                sh 'ls'
            }
        }
    }
}
