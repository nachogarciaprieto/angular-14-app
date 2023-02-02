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

    stage('SonarQube analysis') {
      steps {
        withSonarQubeEnv(credentialsId: "sonarqube-credentials", installationName: "sonarqube-server"){
          sh 'npm run sonar'
        }
      }
    }

  }
}
