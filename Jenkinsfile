pipeline {
  agent any
  stages {
    stage('CheckoutCode') {
      steps {
        git(url: 'https://github.com/Ashraf1507/DevSecOps_App', branch: 'master')
      }
    }

    stage('Log') {
      parallel {
        stage('Log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Unit Tests') {
          steps {
            sh 'cd DevSecOps_App && npm i && npm run test:unit '
          }
        }

      }
    }

  }
}