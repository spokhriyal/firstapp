pipeline {
  agent { label 'Jenkins-Agent' }
  tools {
    
  }
  stages {
    stage("Cleanup Workspace") {
      steps {
        cleanWs()
      }
    }

    stage("Checkout from SCM") {
      steps {
        git branch 'main', ulr: ''
      }
    }

    stage("Build Application") {
      steps {
        sh "dotnet build"
      }
    }
  }
}
