pipeline {
  agent any
  stages {
    stage('AWS Credentials') {
      steps {
        withCredentials() {
          sh """
            mkdir -p ~/.aws
            echo "[default]" > ~/.aws/credentials
            echo "[default]" > ~/.boto
            echo "aws_access_key_id = ${AWS_ACCESS_KEY_ID}" >> ~/.boto
            echo "aws_secret_access_key = ${AWS_SECRET_ACCESS_KEY}" >> ~/.boto
            echo "aws_access_key_id = ${AWS_ACCESS_KEY_ID}" >> ~/.aws/credentials
            echo "aws_secret_access_key = ${AWS_SECRET_ACCESS_KEY}" >> ~/.aws/credentials
          """
        }
      }
    }
    stage('Create EC2 instance') {
      steps {
        sh 'echo "Ansible"'
      }
    }

  }
}
