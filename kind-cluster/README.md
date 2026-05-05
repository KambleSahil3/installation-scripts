# kind-cluster

Local Kubernetes cluster setup using [kind](https://kind.sigs.k8s.io/) (Kubernetes IN Docker).

## Cluster Config

- 1 control-plane node
- 2 worker nodes
- Kubernetes version: `v1.35.0`
- Port mapping: `localhost:8080` → `containerPort:30080`

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [kind](https://kind.sigs.k8s.io/docs/user/quick-start/#installation)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)

## Usage

**Create cluster**
```bash
kind create cluster --config kind-config.yml
```

**Set kubectl context**
```bash
kubectl cluster-info --context kind-kind-cluster
```

**Delete cluster**
```bash
kind delete cluster --name kind-cluster
```
