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
    stage('DockerHub Credentials') {
            steps {
                withCredentials([
                    usernamePassword(
                        credentialsId: 'JENKINS_CREDENTIALS',
                        usernameVariable: 'DOCKERHUB_USERNAME',
                        passwordVariable: 'DOCKERHUB_PASSWORD'
                    )
                ]) {
                    echo "DockerHub Username: ${DOCKERHUB_USERNAME}"
                    echo "DockerHub Password: ${DOCKERHUB_PASSWORD}"
                }
            }
        }
  }
}
