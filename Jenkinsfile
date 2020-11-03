pipeline {

  agent { label 'kubepod' } 

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/venkip41/jenKub.git' , branch:'test'
      }
    }

    stage('Deploy APP') {
      steps {
         script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

 }
}
