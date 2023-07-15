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
        sh '''./mvn clean verify sonar:sonar \\
  -Dsonar.projectKey=petclinic \\
  -Dsonar.projectName=\'petclinic\' \\
  -Dsonar.host.url=http://172.31.7.103:9000 \\
  -Dsonar.token=sqp_97c3948a26b74993e9da8cd7ae6e3ca1cf0be6e9'''
      }
    }

  }
}