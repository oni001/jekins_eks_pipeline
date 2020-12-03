pipeline {

  
  agent {label 'master'}

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/oni001/jekins_eks_pipeline.git', branch:'test-deploy-stage'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}
