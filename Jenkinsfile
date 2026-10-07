pipeline{
  agent any
  parameters {
        string(name: 'FIRST_NAME', defaultValue: 'ANIL')
        string(name: 'LAST_NAME', defaultValue: 'DOLLOR')
    }
  stages{
    stage('Stage 1'){
      steps{
        sh "echo hello ${FIRST_NAME} ${LAST_NAME}"
      }
    }
  }
}
