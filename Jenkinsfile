pipeline {
  agent any
  environment {
    APPSYSID = '680d77352fbcc110ec13ffecf699b69a'
    BRANCH = "${BRANCH_NAME}"
    CREDENTIALS = '18be2029-2e62-4070-8828-dbb3aa39f0f0'
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
