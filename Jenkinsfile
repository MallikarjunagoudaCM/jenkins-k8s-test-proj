pipeline {
  agent none
  stages{
    stage ('Test') {
      agent {
                label "Linux_VM"
                }
      steps {
        sh "whoami"
       sh "kubectl apply -f deploy.yml"
      }
    }
  }
}
