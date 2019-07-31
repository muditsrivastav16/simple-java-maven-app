pipeline {
  agent any
  stages {
    stage ('Compile') {
      steps {
        batchFile 'mvn clean compile'
        batchFile 'mvn test'
        batchFile 'mvn deploy'
      }
    }
  }
}
