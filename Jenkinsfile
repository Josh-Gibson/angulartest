pipeline {
//   environment {
//     NPM_CONFIG_CACHE = "${WORKSPACE}/.npm"
// }
  agent any
  
  triggers {
    githubPush()
  }
    //agent { docker { image 'node:20.11.1-alpine3.19' } }
  tools {nodejs "nodetest"}  //name should be similar to name used for installer in the global tool configuration.

    stages {
        stage('build') {
            steps {
                sh 'echo hewo'
              sh 'node -v'
              sh 'npm install'
              sh 'ng build'
            }
        }
    }
}
