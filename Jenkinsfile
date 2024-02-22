jspipeline {
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
        git branch 'main', ulr: 'https://github.com/spokhriyal/firstapp.git'
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
