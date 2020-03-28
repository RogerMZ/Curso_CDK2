pipeline {
  agent any
  stages {
    stage('Inicio') {
      steps {
        echo 'Inicializando variables y entorno'
        sleep 2
      }
    }

    stage('Build') {
      parallel {
        stage('Tools Information') {
          steps {
            sh 'env'
            sh 'node --version'
          }
        }

        stage('Check FS') {
          steps {
            sh 'ls -ltr'
          }
        }

      }
    }

  }
}