# kubernetes Installation requirements

Before starting, the following conditions must be met to deploy Kubernetes cluster machines:

1. One or more machines, operating system CentOS7.x-86_x64  
2. Hardware configuration: 2GB or more RAM, 2 CPU or more CPU, hard disk 30GB or more  
3. You can access the external network, you need to pull the mirror image, if the server cannot access the Internet, you need to download the mirror image in advance and import it to the node.  
4. Swap partition is prohibited  

# Prepare the environment
The code for setting up the environment has been written in the Prepare the environment folder.

# Install Docker/kubeadm/kubelet on all nodes
This part of the code has been written in the Install kubernetes folder.

# Deploy Kubernetes Master
This part of the code has been written in the deploy folder.

# The deployment process can use the following code to view the image pull process
The test code has been written in the Test folder.

# yaml file
In k8s cluster, resource management and resource object arrangement and deployment can be solved through declaration style (YAML) files, that is, the operations on resource objects can be edited into YAML format files. We call this file a resource manifest file. The kubectl command can directly use the resource manifest file to arrange and deploy a large number of resource objects.  

Commonly used yaml files have been written in the yaml folder.
