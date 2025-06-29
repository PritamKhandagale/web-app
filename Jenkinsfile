pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/your-username/simple-web-app.git'
      }
    }

    stage('Install Dependencies') {
      steps {
        sh 'pip install -r requirements.txt'  // or `npm install`
      }
    }

    stage('Run Tests') {
      steps {
        sh 'pytest tests/'  // or `npm test`
      }
    }

    stage('Archive Results') {
      steps {
        archiveArtifacts artifacts: '**/*.py', allowEmptyArchive: true
      }
    }
  }
}
