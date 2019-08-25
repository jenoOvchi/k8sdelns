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

- Install jq (https://stedolan.github.io/jq/download/)

- Download k8sdelns sources
```bash
curl -Lo k8sdelns-v1.1.tar.gz https://github.com/jenoOvchi/k8sdelns/archive/v1.1.tar.gz
```
- Extract k8sdelns sources
```bash
tar -zxvf k8sdelns-v1.1.tar.gz
```

- Add execution permission to k8sdelns script
```bash
cd k8sdelns-1.1/
chmod +x k8sdelns
```
- Move k8sdelns script to /usr/local/bin/
```bash
sudo mv k8sdelns /usr/local/bin/
```
- Delete k8sdelns sources
```bash
cd ..
rm -rf k8sdelns-v1.1/
rm v1.0.tar.gz
```

## Usage
Execute k8sdelns script with your namespace name (for example "test"):
```bash
k8sdelns test
```
