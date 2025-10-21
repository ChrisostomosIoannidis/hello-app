
pipeline {
  agent any
  environment {
    NODEJS_HOME = tool name: 'node20', type: 'jenkins.plugins.nodejs.tools.NodeJSInstallation'
    PATH = "${NODEJS_HOME}/bin:${env.PATH}"
  }
  stages {
    stage('Install')  { steps { sh 'npm ci' } }
    stage('Build')    { steps { sh 'npm run build' } }
  }
}
