# k8sdelns
Tool for force deletion of Kubernetes namespaces

# Description

If your Kubernetes cluster namespace stuck in the "Terminating" state you can use this tool for its fast forced deletion

## Prerequisites

```bash
$ k create ns test
namespace/test created
$ kubectl delete ns test
namespace "test" deleted
$ kubectl get ns
NAME                  STATUS        AGE
default               Active        66d
kube-node-lease       Active        66d
kube-public           Active        66d
kube-system           Active        66d
kubectl-debug-agent   Active        23h
test                  Terminating   43s
```

## Installation

- Download k8sdelns script
- Add execution permission to k8sdelns script
```bash
chmod +x k8sdelns
```
- Move k8sdelns script to /usr/local/bin/
```bash
sudo mv k8sdelns /usr/local/bin/
```

## Usage
Execute k8sdelns script with your namespace name (for example "test"):
```bash
k8sdelns test
```
