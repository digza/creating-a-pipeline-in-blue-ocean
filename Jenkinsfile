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

    stage('Test') {
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }

    stage('Deliver') {
      steps {
        sh './jenkins/scripts/deliver.sh'
        input 'Finished using the web site? (Click "Proceed" to continue)'
      }
    }

    stage('end') {
      steps {
        sh './jenkins/scripts/kill.sh.'
      }
    }

  }
  environment {
    CI = 'true'
  }
}