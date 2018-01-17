pipeline {
  agent any
  stages {
    stage('Test Pre-Requisites') {
      steps {
        echo 'Test System'
      }
    }
    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            echo 'Deploy Step 1'
          }
        }
        stage('Database Deployment') {
          steps {
            echo 'Deploy Database'
          }
        }
        stage('Deploy Web Application') {
          steps {
            echo 'Deploy Web Application'
          }
        }
      }
    }
    stage('Validate') {
      steps {
        echo 'Perform Validation'
      }
    }
    stage('Clean-up') {
      steps {
        echo 'Perform Clean-up'
      }
    }
  }
}