# K8S-Cluster-Setup - This script only works on Ubuntu 20.04!

## Master Node
```
sudo -i bash <(curl -s https://github.com/AnthonyMacle/K8S-Cluster-Setup/blob/main/install-master.sh)
```
Take note of the "kubeadm join" link

## Worker Node
```
sudo -i bash <(curl -s https://github.com/AnthonyMacle/K8S-Cluster-Setup/blob/main/install-worker.sh)
```

Use the "kubeadm join" in order for the Worker Nodes to join the cluster.

```
kubectl get nodes
```

## Debug 

# From Master Node
```
kubectl drain WORKER-NODE-NAME
```
```
kubectl delete node WORKER-NODE-NAME
```


# From Worker Node

```
 apt-get remove --purge kubelet kubeadm kubectl
```
```
 rm -rf /etc/systemd/system/kubelnet.service.d
 rm -rf /etc/kubernetes/
 rm -rf /var/lib/kubelet/
 rm -rf /usr/libexec/kubernetes
```
```
apt-get install kubelet kubeadm kubectl 
```
Add the node to the cluster:
`
kubeadm join  xxxxxxxxxx YOU NEED TO GET THIS COMMAND FROM THE MASTER NODE -> See below step

# Get join command from Worker Node

```
 kubeadm token create --print-join-command
```


