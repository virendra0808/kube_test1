pipeline {

  environment {
    dockerimagename = "virendra0808/nodeapp1"
    dockerImage = ""
  }

  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git 'https://github.com/virendra0808/test1.git'
      }
    }

    stage('Deploying App to Kubernetes') {
      steps {
        script {
          kubernetesDeploy(configs: "deployment.yml", kubeconfigId: "newjenkins")
        }
      }
    }

  }

}
