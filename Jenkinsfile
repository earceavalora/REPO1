pipeline {
  agent any

  environment {
    VERACODE_CLI_VERSION = "2.16.0"
  }

  stages {
    stage('Preparación') {
      steps {
        echo "Pipeline iniciado. Veracode CLI version definida: ${VERACODE_CLI_VERSION}"
      }
    }
  }
}
