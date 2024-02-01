podTemplate(yaml: '''
apiVersion: v1
kind: Pod
metadata:
  namespace: jenkins
spec:
  containers:
  - name: hello-k8
    image: paulbouwer/hello-kubernetes:1.8
''') {
    node(POD_LABEL) {
        container('hello-k8') {
           echo POD_CONTAINER
           sh 'hostname'
        }
    }
}
