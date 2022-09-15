pipeline {
  agent any

  tools {nodejs "{your_nodejs_configured_tool_name}"}

  stages {
    stage('Install Postman CLI') {
      steps {
        sh 'curl -o- "https://dl-cli.pstmn.io/install/linux64.sh" | sh'
      }
    }

    stage('Postman CLI Login') {
      steps {
        sh 'postman login --with-api-key $POSTMAN_API_KEY'
        }
    }

    stage('Running collection') {
      steps {
      }
    }

    stage('Running api linting') {
      steps {
        sh 'postman api lint'
      }
    }
  }
}