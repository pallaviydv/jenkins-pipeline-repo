pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        bat 'build'
      }
    }

    stage('test1') {
      parallel {
        stage('test1') {
          steps {
            bat 'test'
          }
        }

        stage('test2') {
          steps {
            bat 'test again'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        bat 'deploy'
      }
    }

  }
}