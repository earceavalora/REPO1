pipeline {
  agent any

  environment {
    VERACODE_CLI_PATH = "C:\\tools\\veracode\\veracode.exe"
  }

  stages {
    stage('Verificar CLI Veracode') {
      steps {
        bat '''
        echo Verificando instalación oficial de Veracode CLI...
        "%VERACODE_CLI_PATH%" version
        '''
      }
    }
  }
}

