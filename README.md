## Kubernetes

- **Node** is a worker machine where containers get launched
- **Cluster** is a set of nodes
- **Master** is a node that watches over the cluster nodes and orchestrates containers on worker nodes
- **Pod** group of one or more containers. By default a pod is only accessible by its internal IP address 
- **Deployment** checks on the health of pod and restarts containers if they terminate. Recommended way to manage creation and scaling of pods
- **Service** A way to expose an application running on k8s pods as a network service

Components:
1. API Server:
Frontend for the k8s. CLIs, users, etc. talk to the API server. The kube api server is on the master node.

2. etcd:
Distributed key-value store. All the information gathered from the worker nodes is stored in the etcd store on master

3. kubelet:
Agent that runs on each node in the cluster, ensures containers are healthy. Kubelet interacts with the master to provide information about the node back to the master and carry out instructions from the master node to the worker nodes

4. Container Runtime:
Underlying software used to run containers. For example: docker

5. Controller:
Responsible for noticing and responding to changes in container state, node state etc.

6. Scheduler:
Responsible for distributing work across nodes. Looks for new containers and assigns them to nodes

### Prerequisites


