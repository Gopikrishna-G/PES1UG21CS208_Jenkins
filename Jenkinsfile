pipeline {
    agent any
    stages {
//        stage('Clone repository') {
//            steps {
//                checkout([$class: 'GitSCM',
//                    branches: [[name: '*/main']],
//                    userRemoteConfigs: [[url: 'https://github.com/Gopikrishna-G/PES1UG21CS208_Jenkins.git']]])
//            }
//        }
        stage('Build') {
            steps {
                build 'PES1UG21CS208-1'
                sh 'g++ main.cp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post{
       failure{
           error 'Pipeline failed'
       } 
    } 
}
