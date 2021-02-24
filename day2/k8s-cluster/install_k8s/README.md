# Install-k8s

3 roles: install-k8s, create-cluster, join-workers;

```
ansible-galaxy init install-k8s

ansible-playbook -i hosts main.yml
```

# role1 install-k8s

instalação do docker, kubelet + kubeadm + kublectl
Necessário adicionar os IPs dos [k8s-master][k8s-workers][k8s-workers:vars], gerados no ./provisioning/hosts

# role2 create-cluster

criação do cluster k8s
após playbook ter criado o cluster, fazer acesso e rodar o comando:

```
kubectl get pods
```

testar criação de nós:

```
sudo kubectl create deployment nginx --image=nginx
kubectl scale deploy --replicas 50 nginx

kubectl get deploy
kubectl explain deploy
```

matar o nó:

```
kubectl delete pods nginx
```

# documentações

https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/

https://kubernetes.io/pt/docs/concepts/cluster-administration/addons/

https://www.weave.works/docs/net/latest/kubernetes/kube-addon/

# em caso de erro de permissão

```
ssh-agent bash
ssh-add sua_chave.pem
```
