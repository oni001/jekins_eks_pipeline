pipeline {

  
  agent {label 'master'}

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/oni001/jekins_eks_pipeline.git', branch:'hello-world'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "app.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}
