pipeline {
  agent none
  parameters{
   booleanParam(name: "isDeployPod" defaultValue: true)
  }
  stages{
    stage ('Test') {
       when {
      expression {
       params.isDeploPod
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
