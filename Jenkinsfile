pipeline {
    agent any
    stages {
        stage('git clone or git pull') {
            steps {
                git url: 'https://github.com/hanee0j/ktjenkins.git', branch: 'master'
            }
        }
        stage('CD using k8s') {
            steps {
                sh'''
                kubectl apply -f testapp.yml
                '''
            }
        }
    }   
}