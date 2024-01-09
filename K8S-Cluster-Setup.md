# K8S-Cluster-Setup

## Master Node

sudo -i bash <(curl -s https://github.com/AnthonyMacle/K8S-Cluster-Setup/blob/main/install-master.sh)

Take note of the "kubeadm join" link

## Worker Node

sudo -i bash <(curl -s https://github.com/AnthonyMacle/K8S-Cluster-Setup/blob/main/install-worker.sh)


Use the "kubeadm join" in order for the Worker Nodes to join the cluster.

```
kubectl get nodes
```

