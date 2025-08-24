pipeline {
  agent any

  triggers { pollSCM('H/2 * * * *') }  // проверка изменений каждые ~2 минуты

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Validate YAML') {
      steps {
        sh 'echo "Listing YAML files:" && ls -1 *.yaml || true'
      }
    }

    stage('Build') {
      steps {
        echo 'Build stage (stub)'
      }
    }

    stage('Test') {
      steps {
        echo 'Test stage (stub)'
      }
    }
  }

  post {
    always {
      echo 'Pipeline finished'
    }
  }
}