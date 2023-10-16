pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Arrow'
      }
    }

    stage('Test S') {
      parallel {
        stage('Test2') {
          steps {
            echo 'Running Test 2'
          }
        }

        stage('Test1') {
          steps {
            echo 'Test 1 P'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        input(message: 'Are you Deploying? ?', ok: 'Yes, i am')
        echo 'Comp'
      }
    }

    stage('notify') {
      steps {
        echo 'comp success'
      }
    }

  }
}