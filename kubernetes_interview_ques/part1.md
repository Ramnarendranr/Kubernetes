1. what is the difference between Docker and kubernetes.
       Docker is a container platform whereas kubernetes is an container orchestration platform.
       We will run docker with commands in cli whereas in kubernetes we have yaml files which contains all the informations.
       Kubernetes has some additional features such as auto scaling, auto healing, exposing to the world with the help of load balancers,clustering which kubernetes doesn't persist.

2. What are the main components of kubernetes architecture.
       Control plane/master node:
               API server
               Scheduler
               etcd
               controller manager
               cloud controller manager (CCM)
       Data plane/worker node:
               kubelet
               kube proxy
               container runtime

3. What are the difference between docker swarm and kubernetes?
       Kubernetes is better suited for large organisations as it offers more scalability, networking capabilities like policies and huge third party ecosystem support.

4. WHat is the difference between docker container or Kubernetes pod?
       A pod in kubernetes is a runtime specification of a container in docker. A pod provides more declarative way of defining using YAML and you can run more than one container in a pod.

5. WHat is the namespace in kubernetes?
       In Kubernetes namespace is a logical isolation of resources, network policies, rbac and everything. For example, there are two projects using same k8s cluster. One project can use ns1 and other project can use ns2 without any overlap and authentication problems.

6. What is the role of Kube proxy?
       Kube-proxy works by maintaining a set of network rules on each node in the cluster, which are updated dynamically as services are added or removed. When a client sends a request to a service, the request is intercepted by kube-proxy on the node where it was received. Kube-proxy then looks up the destination endpoint for the service and routes the request accordingly.
Kube-proxy is an essential component of a Kubernetes cluster, as it ensures that services can communicate with each other.

7. What are the different types of services within Kubernetes?
       There are three different types of services that a user can create.
                1. Cluster IP Mode - no one has access except who has access to kuberenetes
                2. Node Port Mode - anyone who has access to any of the worker nodes, say EC2 instances, or VPC access.
                3. Load Balancer Mode - anyone who has access to internet can access

8. What is the difference between NodePort and LoadBalancer type service ?
       When a service is created a NodePort type, The kube-proxy updates the IPTables with Node IP address and port that is chosen in the service configuration to access the pods.
       Where as if you create a Service as type LoadBalancer, the cloud control manager creates a external load balancer IP using the underlying cloud provider logic in the C-CM.
       Users can access services using the external IP

9. What is the role of Kubelet ?
       Kubelet manages the containers that are scheduled to run on that node. It ensures that the containers are running and healthy, and that the resources they need are available.
       Kubelet communicates with the Kubernetes API server to get information about the containers that should be running on the node, and then starts and stops the containers as needed to        maintain the desired state. It also monitors the containers to ensure that they are running correctly, and restarts them if necessary.

10. Day-to-Day activities on kubernetes.
        explain what kubernetes does and for what it is used
