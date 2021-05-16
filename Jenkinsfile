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
                label "master"
                }
      steps {
        sh "whoami"
       kubernetesDeploy(configs: "deploy.yml" , kubeconfigId: "mykubeconfig")
      }
    }
  }
}
