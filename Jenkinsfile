pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('static analysis') {
      steps {
        sh '''./mvnw sonar:sonar \\
  -Dsonar.host.url=http://172.31.7.103:9000/ \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.login=sqp_cdc961205eb429374d9d007f6a9860fc3f7a8491'''
      }
    }

  }
}