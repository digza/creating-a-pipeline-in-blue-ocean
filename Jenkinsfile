pipeline {
  agent {
    docker {
      image 'node:12'
      args '-p 5000:5000'
    }

  }
  stages {
    stage('Test') {
      steps {
        sh 'npm i'
      }
    }

  }
}