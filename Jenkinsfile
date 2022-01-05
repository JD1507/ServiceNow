pipeline {
  agent any
  
  environment {
    DEVENV = 'https://dev76270.service-now.com'
    CREDENTIALS = 'bf228170-dfd6-4771-b372-8dc5fd5ad2ca'
  }

  stages {
   /* stage('full-scan') {
      steps {
        snInstanceScan(
          url: "${DEVENV}",
          credentialsId: "${CREDENTIALS}",
          scanType: 'fullScan')
      }
    }*/
   stage('point-scan') {
       steps {
         snInstanceScan(
           url: "${DEVENV}",
           credentialsId: "${CREDENTIALS}",
           scanType: 'pointScan',
           targetTable: 'incident',
           targetRecordSysId: '3958a00f2f400110ec13ffecf699b6dd')
       }
    }
   /* stage('combo-scan') {
      steps {
        snInstanceScan(
          url: "${DEVENV}",
          credentialsId: "${CREDENTIALS}",
          scanType: 'scanWithCombo',
          comboSysId: '12ff94c51b9fa050b54e85d5604bcbc6')
      }
    }
    stage('suite-scan-scoped-apps') {
      steps {
        snInstanceScan(
          url: "${DEVENV}",
          credentialsId: "${CREDENTIALS}",
          scanType: 'scanWithSuiteOnScopedApps',
          suiteSysId: 'fc8d84891b5fa050b54e85d5604bcb6f',
          requestBody: '{app_scope_sys_ids:["9058fcaa1bc36810b54e85d5604bcb12","4de70218db3a6810f0eb52c8dc961979"]}')
      }
    }
    stage('suite-scan-update-sets') {
      steps {
        snInstanceScan(
          url: "${DEVENV}",
          credentialsId: "${CREDENTIALS}",
          scanType: 'scanWithSuiteOnUpdateSets',
          suiteSysId: 'fc8d84891b5fa050b54e85d5604bcb6f',
          requestBody: '{update_set_sys_ids: ["0f4ccd0ddb9f10108552ff561d961923","3dfac1fddbf9a4d0f0eb52c8dc9619b2"]}')
      }
    }*/
  }
}
