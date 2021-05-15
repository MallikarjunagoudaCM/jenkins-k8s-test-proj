pipeline {
  agent none
  stages{
    stage ('Test') {
      agent {
                label "Linux_VM"
                }
      steps {
        sh "whoami"
       kubernetesDeploy(configs: "deploy.yml" , kubeconfigId: "mykubeconfig")
      }
    }
  }
}
