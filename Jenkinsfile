pipeline {
  agent none
  stages{
    stage ('Test') {
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
