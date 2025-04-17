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

stage('Escaneo estático Veracode') {
  steps {
    bat '''
    echo Iniciando escaneo real con Veracode CLI...
    "%VERACODE_CLI_PATH%" scan --type directory --source . --format table
    '''
  }
}

  }
}

