pipeline {
  agent any
  triggers {
    cron('H * * * *')
  }
  stages {
    stage ('Compile') {
      steps {
        batchFile 'mvn clean compile'
      }
    }
    stage ('Test') {
      steps {
        batchFile 'mvn test'
      }
    }
  }
  post {
    always {
      emailext (
 //       subject: "Job '${env.JOB_NAME} ${env.BUILD_NUMBER}'",
 //       body: """<p>Chcek console output at <a href="${env.BUILD_URL}">${env.JOB_NAME}</a></p>""",
        to: "2015pcecsmudit@poornima.org"
 //       from: "2015pcecsmudit@poornima.org"
        )
    }
  }
}
