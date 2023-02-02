pipeline{
  agent {
    node {
      label 'nodejs-nodo'
    }
  }

  stages {
    stage('NPM build') {
      steps {
        script {
          sh 'npm install'
          sh 'npm run build'
        }
      }
    }
  }
}
