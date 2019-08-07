pipeline {
  agent {
    node {
      label 'Ubuntu'
    }
  }
  
  triggers {
    cron('H * * * *')
    pollSCM('H * * * *')
  }
  
  stages {
    stage ('Compile') {
      steps {
        sh 'mvn clean compile'
      }
    }
    stage ('Test') {
      steps {
        sh 'mvn test'
      }
    }
  }
  post {
    always {
      emailext (
        subject: "Job '${env.JOB_NAME} ${env.BUILD_NUMBER}'",
        body: """<p>Chcek console output at <a href="${env.BUILD_URL}">${env.JOB_NAME}</a></p>""",
        to: "2015pcecsmudit@poornima.org",
        from: "2015pcecsmudit@poornima.org"
        )
    }
  }
}
