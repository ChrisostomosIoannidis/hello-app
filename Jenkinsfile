pipeline {
  agent any
  environment {
    NODEJS_HOME = tool name: 'node22', type: 'jenkins.plugins.nodejs.tools.NodeJSInstallation'
    PATH = "${NODEJS_HOME}/bin:${env.PATH}"
  }
  stages {
    stage('Check versions') { steps { sh 'node -v && npm -v' } }
    stage('Install') { steps { sh 'npm ci' } }
    stage('Build')   { steps { sh 'npm run build' } }
  }
}
