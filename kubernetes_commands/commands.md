minikube start 

kubectl apply -f pod.yaml
kubectl get pods
kubectl get pods -o wide
kubectl get deploy
kubectl delete <podname>
kubectl get all
kubectl get all -A
kubectl describe

minikube ssh
curl and ip of the pod (kubectl get pods -o wide)
