# Kubernetes cluster setup ansible role  
Thist role setups a multi master kubernetes cluster using a loadbalancer.  

## Vars

```yaml
domain_unavailable: true # In case you don't have a domain.
lb_domain: "lb.mammad.k8s" # The address of the loadbalancer

reset_node: false # If need to reset a node (worker or master) set this to True for that specific host

bootstrap_master_node: false # The first time cluster is initialized set this only for the first master

new_master_node: false # Use for join a new master set it to True for that master node
new_worker_node: false # Use for join a new worker set it to True for that worker node
```


## Tags
- `install_containerd`: Install and config containerd as CRI.  
- `reset_cluster`: Use to reset a node (in combination with `reset_node` var)(also a `never` tag).  
- `install_kubeadm`: Install kubeadm, kubectl, and the kubelet on the node.  
- `init_master`: Initialize a kubernetes cluster using kubeadm on the first master in inventory (in combination with `bootstrap_master_node` var)(also a `never` tag).  
- `join_master`: Joins new master nodes to cluster (in combination with `new_master_node` var).
- `create_config`: Runs the commands to copy config for use of kubectl.  
- `setup_cni`: Setups flannel as the CNI for the cluster.  
- `join_workers`: Joins new worker nodes to cluster (in combination with `new_worker_node` var).
- `argocd`: Setups argocd in cluster.
