**SERVICE - svc**

**Why do you need service in kubernetes?**

eventhough Deployment.yaml solves the problem of autoscaling, the ip address will be difference once the pods come up. 

for example:
deployment -> replicas set(rs) -> pods
you have 3 rs- 3pods

pod 1 has 172.109.8.9
pod 2 has 172.109.9.0
pod 3 has 172.109.9.1

if pod 1 is deleted accidentally and because of rs it comes up with different ip, say 172.109.9.2. but the user/tester tries to access this pod with old ip, it will not work.
To overcome this issue, kubernetes has a **service**.

**What service does in kubernetes?**
1. Load balancer
2. service discovery - instead of ip, gives **labels and selectors**
3. expose to world - allows application to access outside the kubernetes cluster

SERVICE:
1. cluster ip - no one has access except who has access to kuberenetes
2. nopeport - anyone who has access to any of the worker nodes, say EC2 instances, or VPC access.
3. Loadbalancer - anyone who has access to internet can access 
