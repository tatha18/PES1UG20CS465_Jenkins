pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh 'g++ ./main/hello.cpp -o PES1UG20CS465'
        build job: 'PES1UG20CS465-1'
      }
    }
    stage('Test') {

      steps {
        sh './PES1UG20CS465'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deployment stage"'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
