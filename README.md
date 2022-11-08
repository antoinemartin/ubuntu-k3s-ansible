K3S Ansible deployment
======================

This simple Ansible playbook will create a local one node cluster using a local 
registry. This works on a Ubuntu 20.04 instance.


Pre-requisites
==============

Not sure here, but at least the user should be sudoer.


Quick-start
===========


To run, issue the following commands:


```console
$ sudo apt install ansible
$ ansible-playbook site.yaml -i inventory
...
$ k3d kubeconfig merge stuart --kubeconfig-merge-default
/home/ubuntu/.kube/config
$ kubectl get nodes
NAME                  STATUS   ROLES                  AGE   VERSION
k3d-stuart-server-0   Ready    control-plane,master   21m   v1.24.4+k3s1
```
