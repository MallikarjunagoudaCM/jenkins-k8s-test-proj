pipeline {
  agent none
  stages{
    stage ('Test') {
      agent {
                label "Linux_VM"
                }
      steps {
       sh "kubectl get pods"
      }
    }
  }
}
