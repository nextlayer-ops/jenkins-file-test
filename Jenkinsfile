pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        echo 'Checkout Main Repository'
      }
    }
    stage('Lint') {
      steps {
        parallel(
          "yaml lint": {
            echo 'yaml lint'
            
          },
          "ansible lint": {
            echo 'ansible lint'
            
          }
        )
      }
    }
    stage('Test') {
      steps {
        echo 'test'
      }
    }
  }
}