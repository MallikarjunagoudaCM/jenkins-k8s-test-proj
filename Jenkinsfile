pipeline {
  agent none
  parameters{
   booleanParam(name: "isDeployPod" , defaultValue: true)
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
        sh "whoami
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
