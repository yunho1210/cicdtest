pipeline {
  agent any
  stages {
    stage('Prepare') {
      agent any
      post {
        success {
          echo 'pull success'
        }

        always {
          echo 'i tried...'
        }

        cleanup {
          echo 'all end '
        }

      }
      steps {
        echo 'clonning repository'
      }
    }

    stage('stepo') {
      steps {
        sleep 3
      }
    }

    stage('dep') {
      steps {
        sh '''echo "test"
'''
      }
    }

  }
  triggers {
    pollSCM('* * * * *')
  }
}