pipeline {
  agent {
    label 'MyNode'
  }
  stages {
    stage ('Configure') {
      publisher {
        mailer('2015pcecsmudit@poornima.org', true, true)
      }
      trigger {
        scm('* * * * *')
      }
    }
  
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
}
