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
            echo 'Run DDL Statments'
            echo 'Run DML Statements'
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
      parallel {
        stage('Validate') {
          steps {
            echo 'Perform Validation'
          }
        }
        stage('Database') {
          steps {
            echo 'Database Validation'
          }
        }
        stage('Web Tier') {
          steps {
            echo 'Web Validation'
          }
        }
      }
    }
    stage('Clean-up') {
      steps {
        echo 'Perform Clean-up'
      }
    }
  }
}