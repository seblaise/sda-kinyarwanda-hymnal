pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/seblaise/sda-kinyarwanda-hymnal', branch: 'main')
      }
    }

    stage('List Contents of dir') {
      parallel {
        stage('List Contents of dir') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Frontend Unit Test') {
          steps {
            sh 'npm i && npm run test'
          }
        }

      }
    }

  }
}