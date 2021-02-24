## Projeto Ansible + AWS + K8S

será instalado um cluster k8s utilizando o Ansible.

# Dividido em fases:

```
1º - Provisionamento: criar as instâncias para o cluster;
2º - Instalação K8S: criação do cluster;
3º - Deploys de aplicação;
4º - Extra;
```

# Provisioning:

Dentro da pasta roles:

```
ansible-galaxy init create-instances

ansible-playbook -i hosts main.yml
```

# Links úteis:

https://docs.ansible.com/ansible/latest/cli/ansible-galaxy.html
https://docs.ansible.com/ansible/latest/collections/amazon/aws/ec2_group_module.html
