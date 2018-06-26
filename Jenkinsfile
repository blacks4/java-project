pipeline {
  agent any

  stages {
    stage('build') {
      steps {
        sh 'ant -f build.xml -v'
        echo 'Building...'
      }
    }

    // stage('Test') {
    //   steps {
    //     echo 'Testing...'
    //   }
    // }
    //
    // stage('Deploy') {
    //   steps {
    //     echo 'Deploying...'
    //   }
    // }
  }
}
