pipeline {
  agent {
    kubernetes {
      yamlFile 'Jenkins-agent-pod.yaml'
      }
    }

    stage('Deploy to Kubernetes') {
      steps {
      container(name: 'kubectl', shell: '/bin/sh') {
        sh "kubectl get pod"
          }
        }
      }
    }
