pipeline {


  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git 'https://github.com/vimallinuxworld13/jenkins-kubernetes-deploy.git'
      }
    }

  

  
    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "deploy.yml", kubeconfigId: "kconfig")
        }
      }
    }

  }

}
