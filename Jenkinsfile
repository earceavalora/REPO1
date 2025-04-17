pipeline {
  agent any

  environment {
    VERACODE_CLI_VERSION = "2.16.0"
  }

  stages {
    stage('Preparación') {
      steps {
        echo "Pipeline iniciado en entorno Windows"
      }
    }

    stage('Descargar Veracode CLI') {
      steps {
        bat '''
        echo Descargando Veracode CLI...
        curl -sSLO https://downloads.veracode.com/securityscan/veracode-cli/v%VERACODE_CLI_VERSION%/veracode-cli-Windows-x86_64.zip
        powershell -Command "Expand-Archive -Path 'veracode-cli-Windows-x86_64.zip' -DestinationPath . -Force"
        veracode\\veracode.exe --version
        '''
      }
    }
  }
}
