pipeline {
  agent any
  environment {
    APPSYSID = '680d77352fbcc110ec13ffecf699b69a'
    BRANCH = "${BRANCH_NAME}"
    CREDENTIALS = 'bf228170-dfd6-4771-b372-8dc5fd5ad2ca'
    DEVENV = 'https://dev76270.service-now.com/'
  }
  stages {
    stage('Build') {
      when {
        not {
          branch 'master'
        }
      }
      steps {
        snApplyChanges(appSysId: "${APPSYSID}", branchName: "${BRANCH}", url: "${DEVENV}", credentialsId: "${CREDENTIALS}")
        snPublishApp(credentialsId: "${CREDENTIALS}", appSysId: "${APPSYSID}", obtainVersionAutomatically: true, url: "${DEVENV}")
      }
    }
  }
}
