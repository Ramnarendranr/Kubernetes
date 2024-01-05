**ALL ABOUT PODS in K8s**

as docker have containers likewise kubernetes has pods.
user has to install applications in pods in kubernetes.

pod -> definition of how to run a container.
pod.yaml file has all cfg that kubernetes needs to do.

YAML:
pod can be sinlge/multiple container
instead of cmd line, putting everything in .yaml file.

standardization.
if group of containers is placed in a single pod, then kubernetes will allow you shared networking, shared storage
this way container A and B can talk to each other using local host.
