pipeline {
  agent {
    docker {
      image 'node:12'
      args '-p 5000:5000'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm i'
      }
    }

  }
}