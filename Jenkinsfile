pipeline {
  agent any

  environment {
    VERACODE_CLI_VERSION = "2.16.0" // Puedes actualizar a la última si es necesario
  }

  stages {
    stage('Preparación') {
      steps {
        echo "Pipeline iniciado. Veracode CLI version definida: ${VERACODE_CLI_VERSION}"
      }
    }

    stage('Descargar Veracode CLI') {
      steps {
        sh '''
          echo "Descargando Veracode CLI..."
          curl -sSLO https://downloads.veracode.com/securityscan/veracode-cli/v${VERACODE_CLI_VERSION}/veracode-cli-Linux-x86_64.zip
          unzip -o veracode-cli-Linux-x86_64.zip
          chmod +x veracode
          ./veracode --version
        '''
      }
    }
  }
}
