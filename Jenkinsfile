pipeline {
  agent none
  parameters{
   booleanParam(name: "isDeployPod" , defaultValue: false)
  }
  stages{
    stage ('Tests') {
       when {
      expression {
       params.isDeployPod
      }
    }
      agent {
                label "Linux_VM"
                }
      steps {
        sh "whoami"
        sh "date"
        sh "kubectl apply -f deploy.yml"
      }
    }
  }
  
  post {
    success { 
    echo "All good!"
    }
    failure{
    echo "Failed!!!"
    }
  }
}
