pipeline {
  agent { label 'Jenkins-Agent' }
  tools {
    nodejs 'Nodejs21.6.2'
  }
  stages {
    stage("Cleanup Workspace") {
      steps {
        cleanWs()
      }
    }

    stage("Checkout from SCM") {
      steps {
        git branch: 'main', url: 'https://github.com/spokhriyal/firstapp.git'
      }
    }

    stage("Install Dependencies") {
      steps {
        sh "npm install"
      }
    }
    
    stage("Build Application") {
      steps {
        sh "npm build"
      }
    }

    stage("Test Application") {
      steps {
        sh "ng test"
      }
    }
  }
}
