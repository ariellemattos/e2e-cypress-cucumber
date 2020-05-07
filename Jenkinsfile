pipeline{
  agent{
    docker{
      image "node:8-alpine"
    }
  }
  stages{
    stage("Build"){
      steps{
        sh "npm install"
        sh "npm install cypress --save-dev"
      }
    }
    stage("Test"){
      steps{
        sh "npx cypress run"
      }
    }
  }
}
