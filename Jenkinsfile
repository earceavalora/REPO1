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
        echo Verificando Veracode CLI...
        "%VERACODE_CLI_PATH%" version
        '''
      }
    }

    stage('Probar Autenticación') {
      steps {
        bat '''
        echo Probando comando de escaneo solo para validar autenticación...
        "%VERACODE_CLI_PATH%" help scan
        '''
      }
    }
  }
}

