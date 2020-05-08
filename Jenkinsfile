pipeline{
  agent {
    // this image provides everything needed to run Cypress
    docker {
       image 'cypress/base:10'
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
