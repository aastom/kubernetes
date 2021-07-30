List Master nodes
```
kubectl get nodes --selector='node-role.kubernetes.io/master'
```
List worker nodes
```
kubectl get nodes --selector='!node-role.kubernetes.io/master'
```

Kubeadm join print command
```bash
   # for both master and worker join commands
   {
      kubeadm init phase upload-certs --upload-certs
      kubeadm token create --certificate-key <key from the above command> --print-join-command
      
   }
   
   
```
