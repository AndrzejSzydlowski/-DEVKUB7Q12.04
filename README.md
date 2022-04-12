# Домашнее задание к занятию "12.4 Развертывание кластера на собственных серверах, лекция 2"
## Конфа (ETCD на Control plane)
```
[all]
node1 ansible_host=51.250.98.0
node2 ansible_host=51.250.106.211
node3 ansible_host=51.250.111.46
node4 ansible_host=51.250.99.218
node5 ansible_host=51.250.108.79
[kube_control_plane]
node1

[etcd]
node1

[kube_node]
node2
node3
node4
node5
[calico_rr]

[k8s_cluster:children]
kube_control_plane
kube_node
calico_rr
```

## CRI


![Снимок12 4 0](https://user-images.githubusercontent.com/72221502/162991225-110fb289-8204-48c7-a7b5-238eb4de7150.JPG)

## Работоспособность
![ответ 12 4 ](https://user-images.githubusercontent.com/72221502/162990226-23388a57-48ce-4c89-9e93-a6e4cb591765.JPG)
