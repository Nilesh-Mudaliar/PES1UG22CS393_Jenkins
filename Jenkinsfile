pipeline {
  agent any
  stages {
//      stage('Clone repository') {
//        steps {
//          checkout([$class: 'GitSCM',
//                    branches: [[name: '/main']],
//                    userRemoteConfigs: [[url: 'https://github.com/Nilesh-Mudaliar/PES1UG22CS393_Jenkins.git']]])
//        }
//      }
    stage('Build') {
      steps {
        build 'PES1UG22CS393-1'
        sh 'g++ ./main/hello.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Deploy') {
      steps {
        sh 'invalid_command' // Command does not exist
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
