pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        bat(script: 'bat', encoding: 'build')
        bat 'echo "build"'
      }
    }

    stage('test1') {
      parallel {
        stage('test1') {
          steps {
            bat 'echo "test"'
          }
        }

        stage('test2') {
          steps {
            bat 'echo "test again"'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        bat 'echo "deploy"'
      }
    }

  }
}