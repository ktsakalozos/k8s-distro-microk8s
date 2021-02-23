## Why should I read this?

There is (too) much information on how to interact and use a Kubernetes cluster but there is almost none on how to setup one from ground up.
This project tries to close this gap. In understanding what a Kubernetes cluster is and how it works you will gain greater understanding on the following:
- Why K8s works the way it does.
- How to use k8s.
- When to opt for a distribution vs setting up your own.
- How to maintain your cluster.


## Kubernetes services

There are two main types of nodes in a Kubernetes cluster the ones hosting the control plane and the woker nodes that serve user workloads.

The kubernetes control plane is made of:
- the API server, that serves the management rest API
- the scheduler, that decides which machine (node) will host what part (pod) of the user workload
- the controller manager, that implements the decisions of the scheduler and the administration

The services on the kubernetes worker (node) are:
- the kubelet, that oversees the container runtime
- the kube-proxy, that does part of the networking among pods

Components that are not part of the kubernetes distribution but are crucial in its function are:
- the datastore, a key-value data store that keeps the state of the cluster, most often this is etcd
- the container runtime, the component driving the, most of the time this is containerd
- the CNI, the component that does the networking between nodes and pods, popular options here are flannel, calico and cilium



