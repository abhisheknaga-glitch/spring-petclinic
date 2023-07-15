pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('static analysisi') {
      steps {
        sh '''./mvnw sonar:sonar \\
-Dsonar.host.url=http://172.31.7.103:9000/ \\
-Dsonar.projectKey=Petclinic \\
-Dsonar.login=sqp_5241530b74c6c4db0da5e6c9bb1dc2b180a4748d'''
      }
    }

  }
}