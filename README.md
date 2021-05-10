# kubernetes

Installation requirements

Before starting, the following conditions must be met to deploy Kubernetes cluster machines:

1.One or more machines, operating system CentOS7.x-86_x64
2.Hardware configuration: 2GB or more RAM, 2 CPU or more CPU, hard disk 30GB or more
3.You can access the external network, you need to pull the mirror image, if the server cannot access the Internet, you need to download the mirror image in advance and import it to the node.
4.Swap partition is prohibited

# The deployment process can use the following code to view the image pull process
kubectl get pods -n kube-system
NAME                          READY   STATUS    RESTARTS   AGE
kube-flannel-ds-amd64-2pc95   1/1     Running   0          72s
