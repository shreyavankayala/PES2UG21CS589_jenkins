pipeline {
  agent any 
  stages {
//   stage('Clone repository') {
//      steps {
//        checkout ([$class: 'GitSCM', 
//        branches: [[name: '*/main']], 
//        userRemoteConfigs: [[url: 'https://github.com/srujanvr5859/PES2UG21CS426_Jenkins']]})
//        }
//   }
      stage( 'Build') {
        steps {
          build 'pes2ug21cs589-1'
          sh 'g++ main.cpp -o output'
      }
    }
      stage ('Test') {
        steps {
          sh './output'
      }
    }
      stage ('Deploy') {
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
