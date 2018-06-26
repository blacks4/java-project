pipeline {
  agent master

  options {
      buildDiscarder(logRotator(numToKeepStr: '2', artifactNumToKeepStr: '1'))
  }

  stages {
    stage('PRINT') {
      steps {
        echo 'PRINT'
      }
    }

    stage('WRITE') {
      steps {
        // echo 'Testing...'
        sh 'echo $BUILD_NUMBER > build_number'
      }
    }

    stage('READ') {
      steps {
        echo 'build_number'
      }
    }
  }

  post {
    always {
      archiveArtifacts artifacts: 'build_number', fingerprint: true
    }

  }
}
