pipeline{
  agent {
    // this image provides everything needed to run Cypress
    docker {
       image 'cypress/base:10'
    }
  }
  stages{
    stage("Build"){
      steps {
        // there a few default environment variables on Jenkins
        // on local Jenkins machine (assuming port 8080) see
        // http://localhost:8080/pipeline-syntax/globals#env
        echo "Running build ${env.BUILD_ID} on ${env.JENKINS_URL}"
        sh 'npm ci'
        sh 'npm run cy:verify'
      }
    }
    stage("Test"){
      steps{
        sh "npx cypress run"  
      }
    }
    
  }
}
