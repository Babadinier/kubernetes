# Tutorial
Source: <https://www.dotnetcurry.com/aspnet-core/kubernetes-for-developers>

## Commands
Start minikube (simple cluster): `minikube start` <br>
Enable kubernetes dashboard: `minikube addons enable dashboard` <br>
Launch dashboard: `minikube dashboard`
<br><br>
Get node: `kubectl get node` <br>
Ask cluster to host container: `kubectl apply -f {name-file}.yaml` <br>
Inspecting logs of the pod's container: `kubectl logs {name-pod}` <br>
Cleanup and remove pod: `kubectl delete -f {name-file}.yaml` or `kubectl delete pod {name-pod}` <br>
Describe pod: `kubectl describe pod {name-pod}` 
<br><br>
Get namespace: `kubectl get namespace`<br>
Get pods of specific namespace: `kubectl get pod -n {name-namespace}`<br>
Get deployment: `kubectl get deployment`
<br><br>
Create nodeport from deployment: `kubectl expose deployment {name-deployment} --port=80 --type=NodePort`<br>
Get service: `kubectl get service {name-service}`<br>
Create a tunnel between the VM of our local cluster to our local machine: `minikube service aspnet-sample-deployment`