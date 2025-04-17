pipeline {
  agent any

  environment {
    VERACODE_CLI_PATH = "C:\\tools\\veracode\\veracode.exe"
    VERACODE_API_KEY_ID = credentials('VERACODE_API_KEY_ID')
    VERACODE_API_KEY_SECRET = credentials('VERACODE_API_KEY_SECRET')
  }

  stages {
    stage('Verificar CLI Veracode') {
      steps {
        bat '''
        echo Verificando instalación de Veracode CLI...
        "%VERACODE_CLI_PATH%" version
        '''
      }
    }

    stage('Autenticación con Veracode') {
      steps {
        bat '''
        echo Configurando Veracode CLI con API Key...
        "%VERACODE_CLI_PATH%" configure --api-key-id %VERACODE_API_KEY_ID% --api-key-secret %VERACODE_API_KEY_SECRET%
        "%VERACODE_CLI_PATH%" whoami
        '''
      }
    }
  }
}
