pipeline{
  agent {
    // this image provides everything needed to run Cypress
    docker {
      image "node:8-alpine"
    }
  }
  stages{
    stage("Build"){
      steps{
        sh "apt-get install libgtk2.0-0 libgtk-3-0 libnotify-dev libgconf-2-4 libnss3 libxss1 libasound2 libxtst6 xauth xvfb"
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
