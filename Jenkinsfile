podTemplate(yaml: '''
apiVersion: v1
kind: Pod
spec:
  containers:
  - name: kubernetes
    image: paulbouwer/hello-kubernetes:1.8
''') {
    node(POD_LABEL) {
        container('kubernetes') {
            echo "Pod Desplegado"
        }
    }
    node(POD_LABEL)
    stage('Comprobando el POD') {
       container('kubernetes') {
           sh "curl hacktonejenkins.jenkins.svc.cluster.local:8080"
       }
    }
}
