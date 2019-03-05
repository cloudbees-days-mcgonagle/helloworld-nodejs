pipeline {
  agent { label 'nodejs-app' }
  options { 
    buildDiscarder(logRotator(numToKeepStr: '2'))
    skipDefaultCheckout true
  }
  stages {
    stage('Say Hello') {
      steps {
      checkout scm
       container('nodejs') {
        echo 'Hello World!'   
        sh 'node --version'
      }
    }
  }
}
