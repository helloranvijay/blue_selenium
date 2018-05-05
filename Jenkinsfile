pipeline {
  agent any
  stages {
    stage('Initialize') {
      agent any
      steps {
        bat 'echo "hello"'
        bat 'cd C:\\Users\\RANVZ\\eclipse-workspace\\Saatvik_I'
        bat 'java -version'
      }
    }
    stage('Execute') {
      steps {
        bat 'C:\\Users\\RANVZ\\eclipse-workspace\\Saatvik_I\\start.bat'
      }
    }
    stage('send email') {
      steps {
        emailext(subject: 'Test Success: $PROJECT_NAME - Build # $BUILD_NUMBER - $BUILD_STATUS:  !', body: '$PROJECT_NAME - Build # $BUILD_NUMBER - $BUILD_STATUS:  Check console output at $BUILD_URL to view the results.  Selenium Script Execution was a success', attachLog: true, from: 'hello@ranvijay.in', replyTo: 'no-reply@ranvijay.in', to: 'hello@ranvijay.in')
      }
    }
  }
}